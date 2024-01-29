---
{"dg-publish":true,"permalink":"/Zettelkasten/14a10a 如何安装OFFICE/","dgPassFrontmatter":true}
---

编号:: 14a10a
标题:: 如何安装OFFICE
创建时间:: 2023-03-05 16:06
up:: [[Zettelkasten/14a10 推荐使用的PE工具\|14a10 推荐使用的PE工具]]
来源:: [使用KMS激活office2019之后变成了office Mondo 2016，请问如何恢复？ - 知乎 (zhihu.com)](https://www.zhihu.com/question/424138036/answer/1564893017)

---
安装部署：[下载 | Office Tool Plus 官方网站 (landian.vip)](https://otp.landian.vip/zh-cn/download.html)
激活工具：[文件 (lanzoux.com)](https://wwx.lanzoux.com/iBu7Fksqpmb)

Office16.0的特点
Office16.0是目前唯一保持功能更新的Office，为Office365、2016、2019、2021、Mondo2016（Office365离线版）等提供基础服务。
- 产品通过证书认证，Office2016=Office16.0+2016证书
- 可以用证书转换切换版本（在Office16.0的产品之间）。但是控制面板不会显示切换后版本的变化，而是继续按安装程序显示。
- 同时启用的多个许可证，功能多的覆盖功能少的。

用Visio的话，要么买正版，要么就必须有VisioPro或者Mondo2016的激活信息。
Mondo 2016是Office16平台的开发人员版（就跟Mondo2013跟Office15关系一样），Mondo的功能权限=365的功能权限，是最高的权限。

在部署前的工作
1.删除老的office套件，如果无法删除，那就使用工具箱的移除功能（不能直接使用）
![attachment/Pasted image 20230306132538.png](/img/user/attachment/Pasted%20image%2020230306132538.png)
2.在激活选项卡中，删除激活信息
![attachment/Pasted image 20230306132611.png](/img/user/attachment/Pasted%20image%2020230306132611.png)
3.重置office设置
![attachment/Pasted image 20230306132651.png](/img/user/attachment/Pasted%20image%2020230306132651.png)

推荐部署设置
![attachment/Pasted image 20230305174342.png](/img/user/attachment/Pasted%20image%2020230305174342.png)

自动安装
按下 Ctrl + Shift + P 打开命令框
- 安装 Microsoft 365 企业应用版（Word, PowerPoint, Excel, outlook, access）
	- `deploy /addProduct O365ProPlusRetail_zh-cn_Bing,Groove,Lync,OneDrive,OneNote,Publisher,Teams /channel Current /downloadFirst`
- 安装 Microsoft 365 企业应用版（Word, PowerPoint, Excel, outlook, access）+ Visio 2016：
	- `deploy /addProduct O365ProPlusRetail_zh-cn_Bing,Groove,Lync,OneDrive,OneNote,Publisher,Teams /addProduct VisioProRetail_zh-cn_Groove,OneDrive /channel Current /downloadFirst`

使用HEU_KMS_Activator激活office
选择智能激活即可，注意退出VPN。