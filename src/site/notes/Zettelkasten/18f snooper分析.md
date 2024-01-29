---
{"dg-publish":true,"permalink":"/Zettelkasten/18f snooper分析/","dgPassFrontmatter":true}
---

编号:: 18f
标题:: snooper分析
创建时间:: 2023-07-25 13:49
up:: [[Zettelkasten/18 轨道交通行业规划及TST的长期方略\|18 轨道交通行业规划及TST的长期方略]]
来源:: 

---
主要功能
 capture the communication telegrams between VCC and other sub-system:
VOBC
SMC
SCS (3GSCS does not support)
NVCC 

- VCC – VOBC 之间
    - 特征
        - vcc发送，vobc回应（vobc不主动）
        - 一个问答完成才会有第二个问答，一个问答持续4个cycle。如果在4个cycle内没有回应，视为丢失。
    - 种类
        - VCC Poll
        - Entry Search
        - filler     把ccot时间和snooper时间关联起来，仅做填补用
- SMC VCC 之间
    - 事件触发，双向
    - 没有报文时，发送filler报文
- NVCC之间
    - 第一次握手
        - vobc配置，进路 ，目的
    - 第二次
        - 响应vcc转变
    - 第三次
    - Channel check telegram
- snooper软件界面
    - 导出  file
    - 黑色是vcc发送，绿色是回应
- vobc分析举例
    - loopid可能一样，但环线号是唯一的
    - VCC Loop Channel Number 是唯一的
    - VHID寻找id
    - Search ID:1022, 1023 高端投入和低端投入（gd0 gd1）
    - poll
        - Type 0
        - Requires VOBC to report vital information, such as position, speed
        - Poll more often 
    - Type 1
        - VOBC reports special message, (arrival at a station, ask deviation)
        - Poll only needed
        - VOBC need report some fault
    - 具体应用
        - tp
            - 低端进入，原点
            - 高端进入，原点=低端进入时的原点+512 position
        - AP,  ato激活
            - 1Active/0Passive
                - 如果vobc先passive，则eb为vcc给出
                - 如果vobc先报告eb吗，则eb由vobc给出
            - 
        - RT   Reply Telegram Type
            - 如果为0，vobc回应类型0的报文
        - VM  最大限速
        - CD  Counting Deriction
            - gd0 往高端
        - vt 
            - 一般为0，设置限速才会有非零数值。


一次故障：

列车投入过程中的CCOT信息：
01:37:25 TRAIN 32 AUTHORIZED FOR TRANSITION AREA （进入转换轨）
01:38:22 TRAIN 32 IN SERVICE (列车停车申请ATO激活)
01:38:27 TRAIN 32 EMERGENCY BRAKE ON （开始自建，分为两部分，一为eb自检，二为vobc切换自检）

目前该阶段存在两个问题
1.在第二次brake off到第三次brake on 之间断开vobc电源，会导致"自检未完成"。此过程中，无法对vobc进行rv命令。
2.此过程中，如果没有司机没有进行操作，则将一直处于自检未完成状态。而在司机做了任意操作后，vcc将报一条ENTRY 112 VH 32 FAILURE PAR = f，这意味着自检结束。如果自动地早一点地报par=f，也不会使得中心一直无法rv该列车。