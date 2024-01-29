---
{"dg-publish":true,"permalink":"/Zettelkasten/14a12 最便宜Linux硬件解决方案/","dgPassFrontmatter":true}
---

编号:: 14a12
标题:: 最便宜Linux硬件解决方案
创建时间:: 2023-07-17 11:43
up:: [[Zettelkasten/14a 台式机组装\|14a 台式机组装]]
来源:: 

---
某宝花10块买一个“随身WiFi”，刷入Ubuntu，用SSH远程连接，但是记得一定要把外壳撬掉然后粘个散热器（哪怕是白萝卜也彳亍），否则会过热

1.白嫖一年的 .pro 域名，支持支付宝/银联验证,（zfb可以卡bug白嫖，验证扣费$1，48小时内自动退还），详细去这位大佬的博客看：https://blog.m78.co/chat/porkbun-pro-truename.html或者去Z-Page (https://nic.zpage.eu)申请个免费二级域，嫌麻烦的可以选这个

2.内网穿透。考虑到极限成本零元购的可能，我选择接入Cloudflare，因为他家自带CDN、CC/DD高防防火墙等实用工具，还支持内网穿透（免费）。白嫖内网穿透详细看https://cloud.tencent.com/developer/article/2013003
当然也可以选择免费的FRP服务，bing按需搜索即可（但稳定性无法保证）

3.启动服务器。嫌麻烦的可以直接用Python3的静态HTTP Server模块：“python -m http.server”（当然第二步就要转发8000端口）；动手能力强的也可以自己配置Nginx和PHP（PHP应该比较卡，记得做好散热）

成果：服务器一台，域名一个，个人网站/自动化脚本执行工具 x1

ps：如果你嫌麻烦不如直接去开个30块一年的bt虚拟主机，不强制备案也不用再买萝卜了，推荐46云（https://www.46yun.com/）