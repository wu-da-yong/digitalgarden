---
{"dg-publish":true,"permalink":"/Zettelkasten/14c2 NAS是什么/","dgPassFrontmatter":true}
---

编号:: 14c2
标题:: NAS是什么
创建时间:: 2023-03-03 17:21
up:: [[Zettelkasten/14c 私有ip和公网ip\|14c 私有ip和公网ip]]
来源:: [【硬件科普】NAS究竟是什么东西？你需要一台NAS吗？_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1kZ4y1F733/?spm_id_from=333.999.0.0&vd_source=bcf798ace50733030b9c7e1fb6a3a349)


---

SATA硬盘的工作原理
SATA控制器在物理层与硬盘设备交互，确认硬盘的速度并建立连线。在链路层建立编码流程，在传输层建立资料封包，在应用层与系统进行交互。

NAS工作流程
用一台小的低功耗电脑装载一堆硬盘，然后接入家庭网络，同时开放这台电脑的局域网磁盘共享，这样局域网的电脑可以通过内网IP访问该电脑的硬盘。再通过端口映射把他挂载到公网上，那就可以通过外网访问到这台电脑的硬盘了。这就是你的私有云盘了。

smb协议
实现不同系统间的磁盘访问

RAID
不同磁盘阵列各有取舍，没有绝对的好坏。