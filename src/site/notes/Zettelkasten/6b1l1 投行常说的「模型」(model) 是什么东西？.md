---
{"dg-publish":true,"permalink":"/Zettelkasten/6b1l1 投行常说的「模型」(model) 是什么东西？/","dgPassFrontmatter":true}
---

编号:: 6b1l1
标题:: 投行常说的「模型」(model)
创建时间:: 2023-07-22 22:52
up:: [[Zettelkasten/6b1l 管理咨询从业者的技能\|6b1l 管理咨询从业者的技能]]
来源:: https://www.zhihu.com/question/27031429/answer/105505212

---

投行或者投资界的[财务模型](https://www.zhihu.com/search?q=%E8%B4%A2%E5%8A%A1%E6%A8%A1%E5%9E%8B&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A105505212%7D)（Financial Model）听起来是不是高大上白富美，然而细究其本质及原理，只有三个字：“Low爆了”。数学原理不超过四则运算，顶多加上[开方](https://www.zhihu.com/search?q=%E5%BC%80%E6%96%B9&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A105505212%7D)和乘法。而且制作工具也非常简单，基本都是Excel。这个领域的Financial Model的复杂性不是体现在理论，而是体现在：
- 商业逻辑清晰：找出核心的假设
- 灵活性强：根据客户或老板需求快速调整，有时候真的是先有结论后有推论
- 胆子大：针对众多不可测的变量敢于进行有量级精度的假设或者瞎猜，物理界有海森堡[测不准原理](https://www.zhihu.com/search?q=%E6%B5%8B%E4%B8%8D%E5%87%86%E5%8E%9F%E7%90%86&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A105505212%7D)，商业界有[鲁智深](https://www.zhihu.com/search?q=%E9%B2%81%E6%99%BA%E6%B7%B1&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A105505212%7D)测不怕原理  

看官不信，看我用实战案例来详细分解（郑重声明，以下的所有截图都是真实投资及交易案例中的Financial Model）。

基本可以这么说，几乎所有的财务模型都是拿Excel做出来的。包括但不限于：
- 偏会计或财务方面：财务三张报表的历史及预测
- 偏项目投资或[项目管理](https://www.zhihu.com/search?q=%E9%A1%B9%E7%9B%AE%E7%AE%A1%E7%90%86&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A105505212%7D)方面：NPV/IRR等模型
- 偏股权及[债券投资](https://www.zhihu.com/search?q=%E5%80%BA%E5%88%B8%E6%8A%95%E8%B5%84&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A105505212%7D)方面：市场规模预测、投资价值预测（DCF及Comparable等等）等等、针对各种股权的回报预测
- 偏交易方面：针对各类金融产品（FX、衍生品等等）的模型估算和执行策略等等。

即使最初不是拿Excel做出来的，到交流层面也是拿Excel在各个决策者之间分享和沟通。这一方面说明Excel的强大，以及在金融和财务相关的Professional Service行业的普及；另一方面也说明，这些行业对新技术运用的滞后。

为了说明这些模型，举一些真实的案例对上述的方面挨个说明。下图是一个真实投资案例的财务模型，其中的重要部分已经在图中列出。

![](/img/user/attachment/a9eb0ca0590abfd74a9d604e025fdcd1_720w.webp.png)

  

其中最重要的有基础的三张[财务报表](https://www.zhihu.com/search?q=%E8%B4%A2%E5%8A%A1%E6%8A%A5%E8%A1%A8&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A105505212%7D)（历史+带各种假设的未来预测），其中一个小技巧是自动配平和检查三张表之间关系的模块。做过三张表的财务及金融人士，一定理解这一步的酸楚。

![](/img/user/attachment/e8f81afcecb574889b399e33e6da75d0_720w.webp.png)

![](/img/user/attachment/55e34178a6262a45685b2d5d616b552a_720w.webp.png)

为了完成对公司业绩的预测，还要对公司所处的市场规模以及公司未来的表现进行预测。下图的概述页面就是完成这个工作。

![](/img/user/attachment/c83bf1516965c378946e4235e25542d3_720w.webp.png)

  

在[回报倍数](https://www.zhihu.com/search?q=%E5%9B%9E%E6%8A%A5%E5%80%8D%E6%95%B0&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A105505212%7D)（X_Cal那一页）的计算中，用到各类DCF或者PE Comparable等常用的模型。下图是另外两个实战的模型，利用WACC和DCF等等去[估值](https://www.zhihu.com/search?q=%E4%BC%B0%E5%80%BC&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A105505212%7D)一个公司的价值。

![](/img/user/attachment/0925fa5defed66ea4630632e9693bbe6_720w.webp)

  

[敏感性分析](https://www.zhihu.com/search?q=%E6%95%8F%E6%84%9F%E6%80%A7%E5%88%86%E6%9E%90&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A105505212%7D)，针对投资人最关心的两大指标（回报倍数和IRR），基于各种最重要的场景进行敏感性分析，包括：投资方式（股权？债券？混合？）、[资产注入](https://www.zhihu.com/search?q=%E8%B5%84%E4%BA%A7%E6%B3%A8%E5%85%A5&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A105505212%7D)的不同形态、未来的PE以及未来的EPS等等。

![](/img/user/attachment/92fe1d0adf04e46f787e2dccd69dadec_720w.webp.png)

在个别复杂的情况，还需要针对Equity或者Loan的不同Class或者Tranche进行拆分然后具体的分析。

![](/img/user/attachment/514692961233968da3d70714d500bd3c_720w.webp.png)

![](/img/user/attachment/9201aeacd27de42be400916b8caf1450_720w.webp)

交易员有时候也会拿Excel来做各种金融产品的价格估算和交易执行策略的安排，虽然看起来简单，但是后台对接着庞大的Bloomberg各类接口以及各大牛逼码农开发的各类超级接口和复杂的[后台逻辑](https://www.zhihu.com/search?q=%E5%90%8E%E5%8F%B0%E9%80%BB%E8%BE%91&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A105505212%7D)。下图提供的是一个针对某外汇的交易策略安排及价格估算。

![](/img/user/attachment/95aad50dc2de998317a4c601c25bda5a_720w.webp.png)