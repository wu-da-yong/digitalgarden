---
{"dg-publish":true,"permalink":"/Zettelkasten/14b5 SSD的特点/","dgPassFrontmatter":true}
---

编号:: 14b5
标题:: SSD的特点
创建时间:: 2023-03-03 16:01
up:: [[Zettelkasten/14b CPU是将电能转化为什么能进行计算的\|14b CPU是将电能转化为什么能进行计算的]]
来源:: [【硬件科普】固态硬盘的缓存是干什么的？有缓存和无缓存有什么区别？](https://www.bilibili.com/video/BV1aF411u7Ct/?spm_id_from=333.999.0.0&vd_source=bcf798ace50733030b9c7e1fb6a3a349)和 [【实测】把游戏安装到固态硬盘究竟有什么意义？对比机械硬盘_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1W4411z7v2/?vd_source=bcf798ace50733030b9c7e1fb6a3a349)

---

SSD硬盘做系统盘，机械硬盘做存储盘
打开某个软件的过程。电脑需要先将exe所需要的数据和环境全部从硬盘拷贝给内存，然后还要把Windows系统的一些数据拷贝到内存当中
把游戏安装到固态硬盘相较于机械硬盘，游戏场景载入速度可提升2~3倍，但是对游戏帧率无任何影响。

运行原理
![Pasted image 20230303194611.png](/img/user/attachment/Pasted%20image%2020230303194611.png)
写入数据时，数据会被主控芯片处理，随后存放在nand闪存颗粒中。读取数据时，主控会在NADA颗粒中找到数据，并通过M.2接口和PCIe总线发送到计算机中的其他设备。

电气特性
- SSD不要大数据量地读写（读写寿命有限）。不要把它当作BT等下载盘！
- SSD不适合作为冷数据备份用途，还是磁带/硬盘等比较合适。SSD的数据会在空置过程中流失，温度越高这个速率越快。周围温度在55度时，只需2周数据就有可能开始丢失。
- SSD挂掉之前会有很多坏块产生，我们需要在发生坏块的时候就开始进行数据迁移。不要等不认盘的时候，就后悔晚矣。