# 聊聊美国科技公司的compensation结构设计

在美国工作一转眼已经四年多了，在硅谷Google工作了一年半多，之后搬到了纽约加入了纽约的一家成长型创业公司Squarespace。加上这几年与身边同行朋友茶余饭后的交流，对美国科技公司的compensation\(薪酬\)结构设计有了较为清晰的了解。大部分刚在美国念完本科或者研究生的中国留学生在这方面所知甚少，导致在offer negotiation的时候吃了哑巴亏。希望这篇文章能起到一点科普作用，帮助读者更好地衡量offer，少走一点弯路。

首先需要明确的一个公式是`Offer = Compensation + Benefits + Growth`。不能一味地只盯着钱看。Benefits包含公司伙食，各种保险政策，休假政策等，不作细举。Growth包含你在这个职位的职业发展前景以及公司整体的成长空间，可以看做是未来价值的折现。但是本文将只会聚焦在Compensation一块介绍。

每个公司的Compensation都是基于本地劳动力市场的行情所决定，同样一个工程师，如果面试Google匹兹堡区域的码农职位和他面试Google旧金山区域的职位最后拿到的Compensation是有不小的区别的，因为旧金山区域对IT人才的需求和竞争明显大于匹兹堡区域，因此雇主必须要付出更高的代价来获取人才。而且美国每个州的税收情况也不同，如果你在西雅图或者奥斯汀找工作，因为你之后不需要像加州人民那样交高达百分之十多的州税，雇主在定compensation的时候也会将这些因素考虑在内。很多公司都会从第三方咨询公司购买行情数据来定位自己的招聘策略所处的位置。比如一个公司定位自己在市场的80% percentile（意味着市场中80%公司对同一职位开出的报价低于该公司的报价），结果发现原来大家都涨上去了，自己跌到70% percentile了，那它就会根据分析报告来相应的调整自己的报价和预算。一个公司percentile定的越高，意味着它的招人成本也更高，但能更大概率地招到更优秀的人才。

细说Compensation的结构，主要分成三部分：基本工资，年终奖金和股票。股票根据公司的发展阶段又分成好几种形态。下面我会逐一介绍他们的作用、形式和需要注意的事项。

### 基本工资 \(Base Salary\)

这是Compensation里最核心的一个数字，它还影响着后文的**年终奖**的计算。基本工资一般根据公司现金流和业务情况按每周、每两周、每月发放，发放时会帮你预缴预计的各种税。 一个公司里每个职位都对应着一个合理的基本工资区间，而且如果设计合理的话相邻级别的职位的工资区间应该会有一定程度的重合。

以X公司为例，它的SWE基本工资分布为：

* Junior SWE: 90K ~ 130K
* Senior SWE: 120K ~ 160K
* Staff SWE: 150K ~ 190K

面试的很重要的一个目的就是定位候选人在该公司的合理level，然后报Offer时基于目标level的区间和候选人的面试综合评价、工作经验、工龄等微调。

读者也许会纳闷为什么一个Senior的基本工资可能竟然会低于一个Junior的！这里有几种情况：

1. 该候选人面试表现非常出色，其他硬性指标也都达标，但是她上一段工作经验未能很好地展示X公司对其Senior SWE的要求，比如说带项目对的经验和能力。X公司对她抱有很大期望，也相信如果她加入X能很快地展示她的能力，希望到时候再对她的level做个调整。所以报Offer时卡了level但松了基本工资，希望能用大包来诱惑该候选人上船。
2. 该候选人面试表现符合X公司Senior的bar，但她上一个工作的title还不是Senior，而且是个比X公司规模小不少的公司，估计平均基本工资低于X公司的水平，于是报Offer给了title bump，但卡一下基本工资。对于该候选人来说，既涨了title又涨了工资，当然很开心。对X公司来说，招到了合适的人也合理地节省了招人成本。

附带一提，不少公司会有一个美国养老金账户401K的match福利，比如说你自己交一点，公司会额外给你交比如5%。这里的5%往往是基于基本工资的5%，所以如果你基本工资越高，在401K里能拿到的公司的match的钱越多。因为401K里的钱在没取出来前是一直不用交税的，所以理论上比用税后的现金去投资能带来更高的长期复合回报率。

### 年终奖 \(Annual Bonus\)

年终奖顾名思义就是每年年末发的一笔一次性奖金，作为对**过去一年**该员工工作的奖励。考虑到美国的节假日传统和税务体系，年终奖一般会来下一年的一月至三月间发放，这样这笔收入就不需要作为当年的个人收入纳税。并不是每个公司的compensation结构里都会有年终奖一项。而且它往往会和员工的基本工资和绩效挂钩。比如说X公司规定一位绩效考评中等的SWE年终奖为基本工资的10%, 而一位绩效出色的SWE年终奖为基本工资的15%。国内大公司发年终奖时往往会按照该业务部门的去年盈利贡献分配年终奖池里的总额，然后再按员工绩效分配到该部门下面的员工，这种做法在美国似乎鲜有耳闻。

发年终奖那段时间也是公司员工流动率很大的一段时间，业内有金三银四之说。有一点值得注意的是，如果你下一个雇主在401K的match比例是比不上你现在的雇主的话，比如新公司只match 10%, 而现公司match 50%， 不妨在发年终奖前的一个月调整你的401K 个人contribution，把年终奖的钱尽可能多地contribute到现公司的401K中，这个小技巧能为你带来几千美元的个人资产增值。

### 股票/限制性股票 \(RSU\)

股票是美国科技公司compensation里不可缺少的一个重要组成部分，俗话说“**要想富，得入股**" 💵。一般上市公司或者Pre-IPO的公司会选择发股票/限制性股票，而处于早期或成长阶段的创业公司会选择发期权（下文会详细展开）。以X公司为例，它给新员工A的Offer里包含了四年总价值十万美元的该公司RSU，term是工作满一年后可以vest 1/4，之后每三个月可以再vest 1/16, 这样四年后该员工就能vest该Offer里面的所有RSU。工作满一年后才能vest被称为“One Year Cliff”，旨在期望员工至少呆满一年。不同公司的term各有异同，比如Amazon的term是第一年5%, 第二年15%，之后每半年20%；Snapchat的term是第一年10%, 第二年20%，第三年30%， 第四年40%。这种越往后权重越大的term往往是雇主在给新员工戴金手铐，想以此让员工呆得很久些，对员工来说不是很公平。遇到这种雇主你就需要想清楚自己预计会在该公司呆多久，然后在谈Offer时最大化那段时间的期望收益。

上面的员工A可能会有这样一个困惑：Offer里只写了RSU的价值，但没写我究竟能拿到多少股数，如果公司股票涨了或者大跌了对我的RSU收入有影响么？一般确认股数发生在该员工入职的那天，按照昨日公司股票收盘价\(或者最近一段时间的平均价，具体根据公司政策而定\)算出该员工Offer上对应的RSU股数。继续以A员工A为例，她入职当天公司收盘价为$10, 所以她四年总价值十万美元的RSU对应的股数为`100000/10=10000`股。在A入职一周年那天，她就能拿到其中的1/4即2500股。如果X公司已经上市，A可以选择当天立即按市场价卖出套现（这是最快的一种套现方式但未必是最优的）。假设那天公司收盘价为$15, 那么A**理论上**获取了`2500*15=$37500`的现金收入。但实际上并不是这么操作的。简单地讲，当你vest RSU时，那笔收入是算作个人基本工资收入类别上税的，假设你个人税率是40%, 你需要预缴`37500*40%=$15000`的个人所得税。大部分公司的做法是直接卖掉你vest的部分股票来cover这个预缴税。在A这个例子里，在她vest当天公司会卖出`15000/15=1000`股，剩下1500股留个A自己决定何时卖出。此时A持有的1500股完全等同于她在Robinhood上当天买的1500股股票，之后基于她的投资盈亏和是否超过一年还要再算一笔资产增值税\(Capital Gain Tax\)😵。

### 期权 \(Option\)

和RSU给你多少就值多少不同，期权的意思是给你一个可以用比较便宜的价格购买一定数量公司股票的选择权。假如你的offer letter上写着 **"10000 stocks with strike price at $1.00"**,  翻译一下就是当你vest这10000股后，假设是五年后，公司的每股估值达到了$11.00, 那么你可以选择用每股$1.00的超低价格购买10000股股票。那你购买的10000股的对你的潜在价值就是`10000*(11-1)=100k`，但这个只是所谓的paper value\(账面价值\)，实际上你一分钱都还没入账！而且还自掏腰包了10000元来行权！根据你exercise当年的收入情况而定，你可能甚至还要为这账面上的100k收益多交一笔称作Alternative Minimum Tax\(AMT\), 详情不作展开，可以参考[这篇文章](https://blog.wealthfront.com/improving-tax-results-stock-options-restricted-stock-grants/)。 在上面的例子里，我们假设了五年后公司还没上市，所以你购买的股票根本卖不出去。假设第九年时，公司总算熬到上市了，过了**六个月**的冷冻期后\(刚上市的公司员工的股票要半年后才能交易\) 那时的股价为$21, 这时早期的员工总算能在一级市场套现了，总计能入账`10000*(21-1)=200k`的收益。当然，这200K资产增值还得交long-term的资产增值税，相比较个人所得税率会低很多，假设20%的话，最后实际落袋的现金收益为`200k*(1-20%)=160k`。我们这里假设了该员工exercise持股超过了一年，但如果没超过一年就卖出了，那么这部分收益就要按照更高的个人所得税率来交税了🤯

加入早期的创业公司风险很高，能被大公司收购已经挺不错的了，能最后挺到上市的少之又少，更多的是中道崩殂。在这种方面极端情况下， 持有option的员工的优势就出来了，因为她可以选择不exercise，这样她就不用承担更大的损失。如果是持有RSU的员工，因为RSU grant时已经交了一波个人所得税，公司倒闭时这些RSU就一文不值了，意味着她凭空多交了那么多个人所得税。

细分地讲，期权常见的形式有ISO \(Incentive stock options\)和Nonqualified stock options \(NQSO\)。早期的创业公司大部分会选择ISO形式，因为ISO相比较NQSO是更具有税收优势的。简单地讲，同样的10000股ISO和NQSO，在你exercise的时候，ISO下你是你是不用交个人所得税或者资产增值税的，在NQSO下你需要为\(现在公司股价-strike price）的增值部分交个人所得税的。NQSO相比ISO的优势在于美国法律规定一年一个员工能收到的ISO形式下的股权奖励价值最多只能有100k，如果超过的话必须要用NQSO的形式。当然这条规定对大部分员工都没啥影响，因为一年100k的股权激励在创业公司里面是个很大的数字了，大部分情况下只有公司的高层才能领到这种包裹。关于ISO和NQSO更细节的对比，我在这就不展开了，感兴趣的读者可以参考[这篇文章](https://blog.wealthfront.com/improving-tax-results-stock-options-restricted-stock-grants/)。

关于期权还有一点必须注意，那就是当员工离开公司时, 很多公司的规定是该员工必须要在离职后三个月内exercise她已经vest的期权，不然就作废重新回收到公司的期权池里。如果该公司发展不错的话，该员工要exercise她的期权一般要自掏腰包准备用于exercise的现金来购买vest的股票，小至几万，多至几十万，要在三个月内拿出这么多现金其实是很有难度的。有些人和下一个雇主谈判让下一个雇主在sign on bonus上多给点来cover这个刚需，有时候甚至能谈到让下一个雇主完全cover你因为跳槽要付出的各种代价。硅谷的一些公司试图改善这种期权金手铐，比如Quora, Pinterest和Coinbase, 他们允许员工在离职后的三年至七年内exercise已经vest的期权，大大减轻了员工离职时的经济负担，也给员工选择合适exercise提供了更长的周期。

### ESPP （员工内部持股计划）

全称Employee Stock Purchase Plan \(ESPP\) ，是不少美国的上市大公司用来激励员工的另外一个方式。简单地说，假设X公司现在股价为$100，员工可以按10%（具体比例因公司而异，最高可至15%）的折扣价买入公司的股票, 一年最多能买入价值25k的股票。如果该员工在买入的当天立即卖出的，相当于一次性收获了10%的收益。当然美国税务局不是吃干饭的, 公司给你的10%折扣对应的价值是要按个人收入所得税交税的，等你卖出股票后还要为增值的部分再交一笔资产增值税\(Capital Gain Tax\)。

和上文的股票、RSU、期权相比，ESPP更接近于401K能match多少比例这样的公司福利，通常情况下并不会给员工带来很大的财富增长空间。如果你真觉得这个公司股票很有潜力，你也大可以在公开市场上直接购买其股票而无需为其工作。RSU、期权则期望员工通过这种激励方式产生主人翁精神，从而更积极地、更有效地参与到公司的建设发展之中。

### Equity Refresh

Equity Refresh是指公司为已经入职的员工提供的奖励更新机制, 这是很少会在Offer letter上提到的但其实非常重要的一个部分。为什么说这个也很重要呢？设想下，X公司给A开出了100K+四年十万美金RSU奖励的Offer，对A来说，未来四年每年的预计收入为`100k+25k=125k`。假设A接了Offer并在X公司开开心心地奋斗了两年，有一天突然意识到那时自己未来四年每年的收益为`(125k, 125k, 100k, 100k)`! 因为再过两年她一开始的RSU全部vest光了！那时任何一个能开出比100K更高Offer的公司对A从经济层面来说都是很有吸引力的，对X公司来说其实是件很不好的事，因为随随便便一个公司就能挖走一个公司里的一个中层顶梁柱。Equity Refresh的作用就在于确保一个员工在任何时间节点上都有足够的经济层面的奖励，不会因为equity快vest完或者已经vest完了就立马拍屁股走人。

具体如何操作呢，这个因人因地因时而已。有些公司会选择在员工雇佣每满一年的那个薪资调整周期\(comp review cycle\) 给该员工在基本工资上有一个merit increase（可以理解为抗通胀，比如3%的增长），然后再新发一笔RSU，同样分四年vest，两者叠加再加上该员工已有的基本工资和RSU，可以确保该员工未来四年的收益是非常有吸引力的。也有些公司在该员工工作满两年或者三年的时才开始进行equity refresh。这些都是值得在谈Offer时问清楚和计算进去的因素。



最后还是再强调一下文章开头的一句话，薪资只是选择一个公司的一部分，还有很多无法量化的因素需要求职者自己量体裁衣地分析比较，最大化自己未来的经济层面的成功和职业道路上的成功。如果你有什么问题，或者有什么想要和其他朋友分享的，请在文章底部留言或者关注我的微信公众号【艺与术】\(various\_\_artists\)私信交流😘

![&#x626B;&#x7801;&#x5173;&#x6CE8;&#x3010;&#x827A;&#x4E0E;&#x672F;&#x3011;&#x5FAE;&#x4FE1;&#x516C;&#x4F17;&#x53F7;](../.gitbook/assets/qrcode.jpg)



**Reference**

1. \*\*\*\*[**https://blog.wealthfront.com/new-college-grad-stock-compensation/**](https://blog.wealthfront.com/new-college-grad-stock-compensation/)\*\*\*\*
2. \*\*\*\*[**https://blog.wealthfront.com/409a/**](https://blog.wealthfront.com/409a/)\*\*\*\*
3. \*\*\*\*[**https://blog.wealthfront.com/stock-options-versus-rsu/**](https://blog.wealthfront.com/stock-options-versus-rsu/)\*\*\*\*
4. \*\*\*\*[**https://blog.wealthfront.com/an-employee-perspective-on-equity/**](https://blog.wealthfront.com/an-employee-perspective-on-equity/)\*\*\*\*
5. \*\*\*\*[**https://www.inc.com/business-insider/tech-companies-employee-turnover-average-tenure-silicon-valley.html**](https://www.inc.com/business-insider/tech-companies-employee-turnover-average-tenure-silicon-valley.html)\*\*\*\*
6. \*\*\*\*[**https://blog.wealthfront.com/improving-tax-results-stock-options-restricted-stock-grants/**](https://blog.wealthfront.com/improving-tax-results-stock-options-restricted-stock-grants/)\*\*\*\*
7. \*\*\*\*[**https://blog.wealthfront.com/good-espp-no-brainer/**](https://blog.wealthfront.com/good-espp-no-brainer/)\*\*\*\*

\*\*\*\*

