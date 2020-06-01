# AMP Email——构建可交互的动态邮件

如果你是Gmail和Google Docs的用户，相信你肯定用过Google Docs的评论及时回复功能：你的同事在你的design doc（设计文档）中留了几个评论，一会后你收到一封邮件提醒，你只需在邮件的回复输入里填写回复并发送即可，从头到尾不需要离开那封提醒邮件即完成了一个任务。

![Source: https://www.blog.google/products/gmail/take-action-and-stay-up-to-date-with-dynamic-email-in-gmail/](../.gitbook/assets/gmail_comment_0gwzkhb.gif)

不知你是否好奇过这是怎么做到的，毕竟我们习以为常的邮件要不是纯文字的，要不就是没有JS加载的静态HTML页面。这背后的技术叫AMP Email，官方网站是[https://amp.dev/about/email](https://amp.dev/about/email/)。先撇开AMP Email不说，AMP （Accelerated Mobile Pages）可能听过或了解的人更多点。它起初是由Google的[Malte Ubl](https://www.linkedin.com/in/malteubl)于15年设计并推广，旨在提高网页的首次加载速度，从而提升手机端的用户体验，毕竟手机浏览器和桌面版相比性能和带宽都受限。AMP作为Google的mobile web的战略性策略之一，利用其搜索引擎老大哥的地位，制定新的游戏规则，给内容商提供一点甜头，进一步巩固它对移动网络内容的创建和分发规则的绝对掌控权。Facebook Instant Articles、Apple News、Baidu MIP都是异曲同工的策略。

技术上来说，AMP简单地讲就是一个阉割版的web component框架，通过提供一套opinionated的组件来代替对native JS的使用需求，再通过服务器端预渲染和Google自家CDN缓存，进一步减少客户端加载时间和渲染时间。AMP Email就是把AMP的那套思路运用到Email这个特殊的互联网文本中，从而实现可交互的动态邮件！撇开Google自身的利益和企图不说，如果这个技术能帮助终端邮件用户获得更好的邮件浏览体验、快速地完成传统的Click To Actions \(CTAs\)，未必不失为一个有价值的技术。

想像下你能在邮件里完成一个医生预约，更新预约，发表就诊体验留言，或者把喜欢的推荐产品加到购物清单里（wishlist），或者查看订单的物流信息，节省了打开多个Tab加载各种不一样的网页来完成一个任务的时间。

在笔者就职的公司Squarepace里，我们每年会有两次Hack Week，就是长达一周的Hacksoon。在Hack Week里，大家可以做自己任何想做的实验和项目，尝试一些新的ideas，大部分最后都不会真正上线，但是通过这种形式可以带动员工的创造性和积极性，以期提高公司整体的产品创造力。在五月末的这次Hack Week里，我尝试了把我们产品中发给用户的部分email转化成AMP Email，希望以此来改善用户体验，从而提高用户对我们的品牌认知。

以礼品卡邮件为例，当一个买家在某个Squarespace商家的网站上买了他们的礼品卡后，礼品卡接收人会收到一封邮件，里面包含了礼品卡金额、卡号、问候语等主要信息。用过礼品卡的朋友可能有过这个痛点，就是一张大额的礼品卡用了一次后放了一段时间，等到想起来再想去用时忘了里面还有多少余额，在美国大型的零售商的礼品卡一般支持打电话或者去官网查询余额。但Squarespace的礼品卡功能目前还不支持买家直接查询余额，现在的唯一途径是假装checkout，输入礼品卡号，在checkout里我们会告诉你礼品卡的余额。可想而知，这并不是理想的用户体验。我们就设想在礼品卡邮件里添加一个礼品卡余额查询模块，这样买家只需打开那份礼品卡邮件就能实时看到里面的余额——看起来非常理想的AMP使用场景！

**References**

* [**https://zhuanlan.zhihu.com/p/42919326**](https://zhuanlan.zhihu.com/p/42919326)\*\*\*\*
* \*\*\*\*[**https://zhuanlan.zhihu.com/p/21741712**](https://zhuanlan.zhihu.com/p/21741712)\*\*\*\*

