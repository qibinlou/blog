# DeFi从入门到精通之Compound——去中心化的货币市场

![Compound Finance](https://static1.squarespace.com/static/5bdbaf425417fcc3b68e463d/t/5f1c48a70f881948c76c88c9/1595689155928/Compound+Finance?format=1000w)

2020年在区块链领域最火的莫过于[\#Defi](https://twitter.com/hashtag/DeFi)了, 全称Decentralized Finance，即去中心化金融。“去中心化”对于有些人来说是个政治气味很浓的词，对于技术极客来说却是个美丽新世界。Permissionless Finance或许是个比较中性的别称。简单地讲就是基于Ethereum智能合约平台之上的金融应用协议，具有透明公开、可审查、不受单一实体控制的特点。现在很火的几个金融产品领域包括Lending（借贷）、Trading（交易）、Derivative（衍生品）。本期【艺与术】专栏我们就来聊一聊Lending领域的领头羊[Compound Finance](https://compound.finance/), 踮起脚尖我们或许能看到未来金融科技的方向。

Compound其实就是个去中心化的货币市场（Money Market\), 对标传统金融行业的产品就是余额宝了：你有一点闲钱，放在银行卡里给银行送钱，存进余额宝里能每天赚点利息；类似的当你有一点加密货币资产比如BTC和ETH，与其闲置在电子钱包里，放进通过Compound协议搭建的货币市场里就能币生币保持资产增值。这些利息是从哪来的呢？货币市场是个双边市场，有资产提供方（Supplier），也有借款方（Borrower），借款方为借得资产付点利息。借款有很多的用途，在传统金融里，我们借钱可以去投资实体经济创业、可以去换之前的贷款、可以加杠杆来放大收益；类似的，Compound的借款方可以用借来的币去加杠杆做多、做空，去投资其他的项目等等。

![Compound&#x8D27;&#x5E01;&#x5E02;&#x573A;&#x4E0A;&#x7684;&#x52A0;&#x5BC6;&#x8D27;&#x5E01;&#x6536;&#x76CA;&#x7387; \(Supply Markets APY&#x4E00;&#x680F;&#xFF09;](https://static1.squarespace.com/static/5bdbaf425417fcc3b68e463d/t/5f1c58e7f6d4d94f9530e826/1595725624914/Compound+Market+rates?format=1000w)

作为投资者最关心的Compound货币市场的年化收益率（APY）是怎么计算的？如果是去中心化的货币市场，谁来负责调整这个收益率来保证市场的有效性？这里就要介绍Compound协议的第一个设计：抵押贷款。比如当你想要借入DAI，你不能空手去借，因为在一个去中心化的全球化匿名网络里，你是没有任何信用的（credit），也就很难完成通常的银行信贷。但你可以抵押你手上的其他资产，比如ETH或者USDC，这样万一发生违约贷款（default loan），系统就能卖掉抵押资产来平仓。在Compound抵押资产的方式就是在Supply Market提供抵押资产，比如存入USDC，不仅能赚1.56%的年化收益，还能获得一定比例的抵押贷款额度。

