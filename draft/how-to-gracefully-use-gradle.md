---
description: 本文将基于Gradle 5.5介绍几个非常实用但鲜为人知的Gradle使用技巧，帮助读者优雅地使用Gradle。
---

# 如何优雅地使用Gradle

## 如何优雅地使用Gradle

Gradle是一个基于Apache Ant和Apache Maven概念的JVM项目自动化建构工具。 有别于传统的不忍卒读的XML项目设置语言，它使用基于Groovy或者Kotlin的DSL\(领域专用语言\)来配置项目构建流程，大大提高了可读性和易用性。Spring Framework、Hibernate等著名的开源框架都在使用Gradle，当然还包括Gradle本身。

当然Gradle本身也是有学习曲线的，很多开发者对其的理解和使用可能只停留在`gradle test`和`gradle build`上。随着项目代码的增加，项目依赖也越来越多，自定义的构建步骤也开始出现，整个项目的构建速度渐渐变慢，进而使得持续集成的速度也相继变慢。

本文将基于Gradle 5.5介绍几个非常实用但鲜为人知的Gradle使用技巧，帮助读者优雅地使用Gradle。

### 使用Gradle Wrapper

Gradle Wrapper是官方推荐的使用Gradle的方式，因为它可以简单地声明要使用的Gradle的版本，然后在项目构建中使用那个指定的版本来跑各个构建任务。这样，不管你用的是命令行还是IDE，不管你用的是Windows还是Linux, 你用的都是同一个命令，比如`./gradlew build`，此处`./gradlew` 即是所说的Gradle Wrapper。

生成Gradle Wrapper，你只需要在项目根目录下运行`gradle wrapper --gradle-version 5.4.1`, 你可以根据需要选择适合你的gradle-version。

### --parallel

随着项目的发展，产品代码和测试代码与日俱增，然而项目的整体构建速度通常都会不断变慢。变慢的原因有很多种，比如有不可避免的编译时间增长，也有可以改善的测试运行方式。Gradle 5.x 版本中已经做了很多优化，比如默认的incremental build\(增量编译\)和build cache\(构建缓存\)。此外，现在大部分电脑都配置了多核CPU，Gradle提供了`--parallel` 功能来帮助你基于多核CPU并行运行Gradle的任务。比如你的项目里有三个无交叉依赖Gradle子模块，当你在一台六核的机器上跑时，三个子模块可以并行编译和运行测试，理论上你最多可以节省2/3的构建时间。

### --fail-fast

在CI\(持续集成\)构建项目时，必不可少的一个环节是跑自动化测试，比如单元测试和集成测试。大型的项目往往有成百上千个自动化测试，如果CI系统没有很好的并行化机制的话， 全部跑完至少要个五到十分钟，甚至更久。万一你的分支里有测试挂了，默认情况下你必须要等到所有测试跑完才能得到反馈（比如收到提醒）。假设那个测试是在第二十秒时就挂了，意味着我们浪费了之后五到十分钟的机器资源。

`--fail-fast` 正是为了解决这个问题而设计的，它的作用就是一旦有测试挂掉就直接终止，还没跑的测试就被跳过了。这样我们的CI环境资源利用率就能有所提高，对于那种有数十个甚至上百个工程师在同时工作的代码库，`--fail-fast`的优化效果就很明显了。

`--fail-fast` 只适用于Gradle Test类别的构建任务，比如 `./gradlew test --fail-fast`。用于其他任务则会报错，比如`./gradlew build --fail-fast`，因为build不是Test类别的任务。除了用于命令行，你还可以在Gradle脚本里设置：

```text
test {
    failFast = true
}
```

### -t, --continuous

`--continuous` 帮助开发者在本地开发时更高效地验证他们的changes。比如你在写一个类的单元测试，你已经有以下的两个文件

```java
# Foo.java
public class Foo {
    public int sum(int a, int b) {
        return a + b;
    }
}

# FooTest.java
public class FooTest {
    @Test
    public void testSum() {
        // TODO: implement me
    }
}
```

你可以在命令行运行`./gradlew test --tests FooTest --continuous` 或者缩减版`./gradlew test --tests FooTest -t`，当你改变`Foo.java`的实现或者`FooTest.java`的测试代码时，Gradle会检测到文件内容改变，从而重新编译运行你的测试，无需你人工执行同样的命令。

这个功能非常适合那些需要快速反馈、迭代、验证修复的任务，比如编译、测试、重构、代码风格错误修复等。

### -x, --exclude-task

当你想执行一系列Gradle构建任务但又想跳过某些很慢的或者是不相关的任务时，`-x`就派上用场了。比如Gradle有个任务叫`check`, 它往往是开发者push本地commits前跑的一个任务，可以看成一个快速代码正确性校验的综合任务，包含编译、代码静态分析、自动化测试等。如果此时你不想跑集成测试，因为集成测试很慢，你就可以在命令行跑`./gradlew check -x integrationTest`, 这样它就会跑除了集成测试之外的相关校验任务。

### -m, --dry-run

当你修改了一些Gradle脚本，或者想快速验证你的Gradle配置是正确的，合理地应用`--dry-run`能帮你节省不少时间。比如你想看看`check`任务到底会跑哪些相关任务时，你可以用`./gradlew check -m`, 不出几秒Gradle就会在命令行打印出需要执行的任务名（但不执行）。

### --offline

设想你在火车或者飞机上很无聊，突然灵光乍现想到一个优化你现在系统的方法，你迫不及待地打开笔记本啪啪啪啪敲完了代码，结果在命令行一跑Gradle报错说没有网络连接，无法下载一些项目依赖。再有没有比这个更让一个工程师痛苦的事了吧。其实Gradle大部分时间都在本地缓存了所有的项目依赖，只是它习惯性地会去网上重新更新校对下依赖版本等信息。此时`--offline`就能帮助你强制Gradle开启离线工作模式!

### api / implementation / ~~compile~~

很多构建系统都会碰到一个棘手的问题：如果合理解决**Transitive Dependency**（依赖传递\)? 比方说现在有如下依赖关系`App -> Lib A -> Lib B`, 如果_Lib B_ 只在_Lib A_的函数内部使用到，理想的情况下_App_的代码是不能直接调用_Lib B_的，因为_Lib B_只是_Lib A_的内部实现方式\(internal implementation\)。 然而大部分情况下你会发现_App_的代码竟然能调用_Lib B_!

以上就是在Gradle脚本里使用`compile`关键词的副作用。不要以为这仅仅是一个内部实现暴露的问题，它还会造成依赖版本解决出错导致应用层出错，还会减慢项目代码的整体编译速度。

Gradle从3.4版本起其实就提供了一个解决方案。它把`compile`语义拆封成两类，`api`和`implementation`。`api`等价于被_deprecated_的`compile`。至于`implementation`, 以上面的例子为基础

```text
# build.gradle of App
dependencies {
   api project('LibA')
}

# build.gradle of Lib A
dependencies {
   api project('models')
   implementation 'com.google.guava:guava:18.0'
}
```

这样_Guava:18_这个内部依赖就不能渗透到_App_那里。如果_App_刚好也需要使用_Guava_, 它就需要显示定义_Guava_为它的依赖，而且它可以自由选择_Guava_的版本而不用担心版本误用或者冲突。

**参考文章**

* [Improving the Performance of Gradle Builds](https://guides.gradle.org/performance/)

