
# 会议纪要：管理会议，2019年7月07日
社区管理会议于北京时间2019年7月07日10点-12点30、在微信群线上召开。

## 社区与会人员有：
天然
Tina
Liu Jie
驴子
Mike
ZT
xinhao
笑脸哥


## 1.1 指数设计

类似期权交易的iv。交易挖矿指数就旁边标注隐含难度

这个指数本质是难度分之一，其他都是常数。

每个随机量一个标的，不要混起来。所以不想带入挖矿手续费，block time等其他变量。

有实际意义的指数在挖矿世界可能会在小数点后面五六个零很不雅观。
常数两个层面，一是赋予实际意义，比如1t挖一天的产出。二是也看起来舒服，是一个小数点之前有三四位的正常数字。

另一个选项是直接用科学记数法来表示，这样把小数点后面的零都放入了科学记数法里面。


## 2.1 GNU/linux以及阿帕奇的组织架构 by Mike

![阿帕奇的思维导图](https://github.com/carboclan/pm/blob/master/notes/images/apache-arch.png)

Apache运营的基本原则：

1精英主义（需要确认是不是meritocracy），主要反映在管理方式上，由各层级的精英小组，对议题进行投票决策，绝大多数人服从执行

——投票为3种，赞成，弃权，反对，投反对票的人，需要提出替补方案，否则反对无效

——精英小组面，投票权相等，没有权重

——任务认领采用类似google，或者说google借鉴了Apache的方式，由精英小组分解并评估任务，项目成员认领，完成后提交并维护，再由精英小组评估完成质量，给出评定


2按贡献值自下而上的晋升机制

——按贡献值进行由用户——》开发者——》提交者——》项目管理委员会 或者 会员——》基金会（ASF）——》董事会（具体贡献值计算方法，可以进一步了解，以衡量执行的效果）

——很少空降，Apache文化也不赞同空降


3基础设施完善

——基金会提供完善的项目管理，技术管理，品牌，公关，法务等服务，保证开发者顺畅参与，而不必为非技术层面的问题困扰

——项目孵化流程高效，Mike认为是Apache基金会的核心流程



面临的问题：

1项目补充新开发资源困难

——相当比例的高评级项目，是由商业组织支持的，比如hadoo由雅虎支持，个人开发者参与不足，导致项目进入Apache孵化流程后，无法补充新开发者，比较尴尬


2决策集中化

——大V抱团，因为会员的晋升，除贡献值外，也依赖于老用户的推荐，且在决策时不分权重，所以容易造成大V抱团，通过对自己有利的决议



讨论汇总：

1需要获得什么样的资源？由谁提供？（Mike）

——需要先回答本组织的目标是什么？实现此目标需要的资源是什么？

——如果目标是个人开发者无法参与的，比如linux基金会，主要是以linux的商业化为目标，依赖于大厂商的参与，所以会员以大厂商为主

——落实到本组织，比如目标是没有难挖的矿，那主要参与者应该是与挖矿产业链相关人员，但这里又分单纯挖矿，单纯交易，挖矿交易三类，需要考虑首先要引入什么资源

——提个思路供参考，比如主要做挖矿金融衍生品，那是不是设计一个通道，把具有金融能力的人，接入挖矿背景的技术团队（类似Tina+刘杰），这样本组织卖点明确，服务方式的设计，也有依据


2开发者参与研发流程是相对明确的，但推广，运营，市场的参与流程是不明确的？（刘杰）

——金融产品需要推广，但具有专业能力的人如何参与？如何计算贡献值，这个流程Apache没有给出范例（刘杰）

——提个思路，建议可计量的推广工作，由参与者承担，但不可计量的推广工作，由全职或兼职工作人员承担，Apache基金会的品牌推广，是这样操作的（Mike）


3 token的经济模型如何设计？（Tina)

——在核心流程的各环节上，做价值捕获，并尝试进行计量(Tina)

—— token的获得如何与组织权益相结合，有收益的同时，也要有荣誉（Mike）





## 2.2 yellow hat dao by tina
相信自由市场奥派做空的人，需要组织联盟，是非主流观点。需要群策群力。

Tina跟几个老外吃饭以后一起提出，成员包括near protocol的创始人乌克兰小哥illia ，曾提出用smart contract做跨连delegate pos，会break所有bft concensus。还有James prestwich设计过hashrate derivative，storj的联创。pow都nichehashable
总之基础设施不安全，需要为基础设施建立有效的市场。
Yellow hat 之于carboclan有点像共产国际&中国共产党。我们是在中国主力干活的组织，外援们也需要有归属，方便大家一起做事

Jie：名字有点怪，白帽黑帽只是tag不是名字，不会这么自称。

## 2.3 文档协作
三个级别的改动
第一层：简单修改直接改
第二层：表述调整就pull request 然后三个人review
第三层：大修改要开会讨论

目前三个人权限，tina 刘杰和天然

提issue要让所有人都看得懂，符合开源社区通用惯例
开源社区标准高于公司

提pull request以后可以再提问评论，
取决于问题级别，来决定要多少人来对这事情决策，小事情一两个人就够了，大事情要让更多人参与


## 进度
2讨论完了，1只讨论了1.1.1和1.1.3，剩余的下次再讨论
下次控制在2小时以内