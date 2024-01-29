---
{"dg-publish":true,"permalink":"/Zettelkasten/14e2c1 vicual studio的初步使用/","dgPassFrontmatter":true}
---

编号:: 14e2c1
标题:: vicual studio的初步使用
创建时间:: 2023-07-19 04:58
up:: [[Zettelkasten/14e2c C语言程序设计\|14e2c C语言程序设计]]
来源:: 

---
### 选择安装C++的桌面开发
![attachment/Pasted image 20220511154858.png](/img/user/attachment/Pasted%20image%2020220511154858.png)

在上面的【工作负载】选项卡，你需要按照你的开发目标选择你需要的VS组件。实现C/C++编程必须配置的工作负载为**“使用C++的桌面开发”**。这套组件已包含生成“桌面应用”——即Windows上**传统的的.exe程序**——必备的所有环境。注意虽然它名字中只提到了C++，但对纯C同样是支持的，编写时注意规范即可（下文会讲）

另一种与此对应的“通用Windows平台 (Universal Windows Platform) 开发”，目标则是新型的UWP应用程序，这是指能够上架Microsoft Store的那种软件，并不是初学者需要的，如果误勾选会浪费10GB+的硬盘空间。



### 新建项目
![attachment/Pasted image 20220511155145.png](/img/user/attachment/Pasted%20image%2020220511155145.png)
在弹出的【新建项目】对话框中，左侧有已安装可供你选择的项目类型，我们展开【Visual C++】这一栏。要编写纯C程序，建议选择【其他】→【空项目】（避免混入不需要的C++依赖）。

### 新建项
![attachment/Pasted image 20220511160106.png](/img/user/attachment/Pasted%20image%2020220511160106.png)
在弹出的【添加新项】对话框中，选择【Visual C++】一栏中的【代码】，你将看到C++项目支持的各种类型的代码文件。常用的C++代码格式是第一个，后缀名为.cpp，这里并没有列出纯C要用的.c格式。
我们需要在底下手动修改文件后缀名，比如把文件名称改为src1.c（啥名字都行，但注意一定要连着后缀名一块改，VS的编译器可以辨认这是纯C代码），然后确认。

### 生成目标程序（也就是Window上最常见的.exe程序）

一般是选择菜单栏中的【生成】→【生成解决方案】

### 无法正常调试
选择我们的项目（注意是那个带两个加号的项目图标，不是解决方案的图标），然后右键，选择【属性】，在属性页左侧展开【链接器】，选择【系统】，将右侧【子系统】项的值修改为“控制台”。确定退出。