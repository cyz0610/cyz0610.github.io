# 物联网导论 第八章 移动通信技术

移动通信技术使得信息的交互不再受到距离的阻隔

完整物联网系统：
- 前端信息生成
- 中间传输网络
- 后端应用平台

出门，钱包、钥匙、钱都不用拿，现在已经可以实现。

## 8.1 移动通信发展历史

无线电话：
- 无绳电话
- 移动电话

移动通信三代的发展：
1. 模拟语音
2. 数字语音
3. 数字语音和数据。

### 8.1.1 第一代移动通信：模拟语音

20世纪20年代到40年代，超外差式无线电接收机。

40年代中期开始，公用移动电话系统（美国、欧洲），1946美国FCC，贝尔系统建立第一个可用于汽车的电话系统，将一个大功率的发射器放在较高的地理位置上，利用单工信道在其覆盖地区接收和发送信号。

20世界60年代，改进移动电话系统（IMTS），也是设在山顶，但有两个频率，一个接收一个发送。

1982年，贝尔实验室发明高级移动电话系统（AMPS），提出*蜂窝单元*。保证相邻单元使用不同的频率，较远的单元使用相同频率，避免频率冲突，可让频率多次使用，充分利用资源。所有基站都会连接到移动电话交换局（MTSO），分层机制。

### 8.1.2 第二代移动通信：数字语音

GSM：
- 运行在多个不同的无线电频率上，用户连接最近的。
- 时分复用技术，多个时槽，供用户不同时间共享。
- 频分复用技术，每一部电话在发送数据的同时，可以另外在一个高50Hz的频率上接收数据。
- 支持自动漫游和自动切换，较强的安全性能和抗干扰能力。
GSM蜂窝大小分为：
	宏蜂窝（楼顶山顶），微蜂窝（市区内），微微蜂窝（室内集中的地方），伞蜂窝（填补蜂窝间的空白区）。
GSM系统后台网络：
	基站系统（包括相关控制器）
	网络交换系统（核心网，衔接各部分）
	GPRS核心网（基于报文的互联网连接，可选）
	身份识别模块（SIM卡）

CDMA：
	码分多址技术，由蜂窝组网、扩频、多址接入以及频率复用技术结合而成，含频域、时域、码域等三位信号处理的一种协作，抗干扰能力好、抗多径衰落、保密安全性高。
	任何时刻、任何频段、从混合信号中提取期望数据，并能拒绝噪声信号。

### 8.1.3 第三代移动通信：数字语音与数据

2.5G：
- HSCSD（高速电路交换数据）（GSM升级版）
- GPRS（分组通信，共享信道资源）
- EDGE（支持更多数据位）

CDMA技术的三个标准：
- IMT-DS,对应W-CDMA（中国联通）
- IMT-MC,对应CDMA2000（中国电信）
- IMT-TD,对应TD-SCDMA(中国移动)和UTRA-TDD

## 8.2 3G通信技术和标准

### 8.2.1 TD-SCDMA

时分-同步码分多址

CDMA系统是一个自干扰系统，具有“呼吸效应”，覆盖半径会随着用户的数目的增加而缩小。

但TD-SCDMA利用低带宽的FDMA和TDMA限制系统的最大干扰，拥有灵活的上下时隙配置，在单时隙中应用了CDMA技术来提高系统容量，还利用联合检测和SDMA技术对客户终端的信号进行跟踪，充分利用下行信号能量最大程度上抑制了用户之间的干扰。TD-SCDMA不在是一个自干扰系统。

TD-SCDMA采用动态的调控功率，解决了“远近效应”，手机终端应当依据自己到基站的通信距离，动态的调控传输功率，减少过剩。

### 8.2.2 W-CDMA

宽带码分多址

最初设计是为了能和现有的GSM网络协同合作，使两者的蜂窝系统可以相互融合，不会因为穿越系统而丢失当前呼叫。

包括FDD和TDD两种工作方式，前者工作覆盖面积较大，可以分离的两个对称频率信道上进行接收和传送工作，后者侧重于业务繁重的小范围。

W-CDMA：有三条可利用的公共控制信道和两条专用信道
- 公共控制信道：
	1. 广播公共控制信道（BCCH），携带系统和小区的特定信息
	2. 寻呼信道（PCH），把消息传送到寻呼区的移动台
	3. 前向接入信道（FACH），把消息从基站送到一个小区内的移动台
- 专用信道：控制信道，
		   业务信道

优点：支持异步和同步的基站运行方式，动态调控多种速率的传输，减少系统的多址干扰，提高系统容量，降低传输功率。

### 8.2.3 CDMA2000

- 第一阶段：CDMA 2000 1X EV-DO，随后的多个版本，在Rev B（B版本）中，在物理层、MAC层和连接层分别增加了一些多载波相关的协议。
- 第二阶段：CDMA 2000 1X EV-DV，具有后兼容性，上行下行速率更快。

## 8.3 移动互联网

视频电话、手机电视（已实现）

### 8.3.3 基于用户情景的服务

两种模式：用户主动提交服务请求，服务商根据消息，返回数据结构。
		 服务提供商直接根据数据更新的情况向用户推送最新消息。

两种模式忽略了用户的所处情景

基于位置的服务（LBS），但随之而来的是隐私保护问题。

### 8.3.4 移动社交网络

### 8.3.5 其他应用

- WAP（无线应用协议） 将Internet内容和数据服务带入到电话终端。

- 移动即时通信 QQ，微信 多终端。

- 手机广告

- 手机游戏

8.4 第四代移动通信系统

TD-LTE 吸纳了很多TD-SCDMA技术元素。
TDD采用时分复用进行双工，FDD采用频分复用进行双工。

FDD上下行链路固定频谱分配，并需要频谱隔离度
TDD不需要成对的频带资源支持，可用目前频谱规划中的散杂频谱资源，灵活性优势明显。

按照无线链路的调制方式分：码分多址和正交频分多址。

MIMO（多输入/多输出）技术，利用天线系统的空间信道特性，同时传入多个数据流，从而提高数据速率和频谱效率。


# 第九章 大数据与海量存储

## 9.1 从网路化存储到数据中心

网络存储体结构分为： 
- 直接附加存储
- 网络附加存储
- 存储区域网络。

每种体系结构都使用到了存储介质（磁带、磁盘、光盘、存储接口）

直接附加存储（DAS），存储系统通过缆线直接与服务器或者工作站相连，系统中有多个硬盘驱动器，与主机总线适配器之间不存在其他网络设备（如路由器、交换机）。

DAS优点：
- 实现了计算机内存到存储子系统的跨越
- 管理容易，成本低，结构简单

DAS通常是孤立的，从而对存储资源利用率低、资源共享能力缺失。

网络附加存储（NAS），文件级的计算机数据存储架构，计算机连接到一个仅为其他设备提供基于文件数据存储服务的网络，NAS包括存储器件（CD、硬盘）和专用服务器。

NAS和DAS区别：
- DAS是一种对已有服务器的简单扩展，并灭有真正实现网络互联。
- NAS则是将网络作为存储实体，更容易实现文件级别的共享。

存储区域网络（SAN），通过网络方式连接存储设备和应用服务器的存储架构，为实现大量原始数据的传输进行了专门的优化。SAN由服务器、存储设备和连接设备组成。

SAN特点：
- 存储共享，可以使用高速网络把信息孤岛进行融合。
- 支持服务器从SAN直接启动，使得新服务器可以访问位于损坏的服务器上的存储空间，从而在不丢失数据的情况下恢复系统的功能。

大型数据中心
	提供高度可靠和安全的海量数据存储，还提供及时、持续的数据服务。

## 9.2 数据中心建设

此处指海量数据存储需求的数据中心。

维基百科：是一整套复杂的设施。不仅仅包括计算机系统和其他与之配套的设备，还包括冗余的数据通信链接、环境控制设备、监控设备以及安全装置。

Google解释：多功能的建筑物，能容纳多个服务器以及通信设备。这些设备放置在一起是因为它们具有相同的对环境的要求以及物理安全上的需求，并且这样放置便于维护。

如何规划？如何升级？

### 9.2.1 选址与布局

因素：建设和运营成本、应用需求、政策优惠、数据中心布局

TLA-942标准：
- 入口室，放置互联网接入点（可多个）
- 主分布区，为核心区域，放置核心路由器以及交换机。
- 水平分布区，水平缆线系统的集中点。
- 设备分布区，放置各种服务器以及其他设备机架和机柜，水平缆线的终点。
- 区段分布区，连接点，增强数据中心在重新配置时的弹性，为独立设别提供场所。
- 主干缆线和水平缆线，提供连接。
- 还有电信室、工作人员办公室、控制中心等辅助区域。

### 9.2.2 缆线系统

有非屏蔽双绞线和屏蔽双绞线。

该标准：
- 主干缆线，使用50纳米μm规格的激光器优化的多模光纤（比单模更高的网速）。
- 水平缆线，是使用具有最高信道容量的传输介质。

### 9.2.3 可靠性分级

根据数据中心的应用需求，分四级。

第一级最简单，仅有一个最基本的服务器室。第四级最严格的。

分级参数主要有：
- 是否具有冗余的能源和降温系统（越严格，冗余组件越多）
- 建设的时间（越严格，建设时间越长）
- 每年停止工作的时间（越严格，每年停止工作时间越短）
- 是否使用架空地板、UPS或者发电机（数据维护时所用）

### 9.2.4 能源系统

由可靠性分级来确定，使用场景：当外部供电意外停止时。

### 9.2.5 降温系统

降温设备、抬高悬空的地板、靠近设备进风口的地方提供冷空气。形成“热”通道和“冷”通道。

## 9.3 数据中心技术

### 9.3.1 Google File System（GFS）

超大规模的数据密集型应用的分布式文件系统。

设计观点：
	组件失效不再被认为是意外，为正常。
	通常以GB为单位衡量文件系统。
	对文件操作具有特定的模式（对大部分文件的修改，不是覆盖原有数据，而是在文件尾追加新数据；几乎不对文件进行随机写操作）。
	应用程序和文件系统API的协同设计提高了整个系统的灵活性（减少一致性要求，引入原子性的追加操作）。

[google file system 系统架构](http://static.open-open.com/lib/uploadImg/20120209/20120209125625_451.jpg)

### 9.3.2 MapReduce

思想借鉴函数式编程语言，两个程序，Map和Reduce，以及一个在计算机集群上执行多个程序实例的框架。

### 9.3.3 BigTable

BigTable是一个稀疏的、分布式的多维有序图。

### 9.3.4 Hadoop

组成部分：提供高吞吐量的分布式系统HDFS，大规模数据集的分布处理MapReduce，对大型表格进行结构化数据存储的可扩展分布式数据库HBase。

## 9.4 典型的数据中心

数据中心选址考虑因素：
	廉价电力成本
	风能、水力等低碳电能的获取，实现低碳排放
	靠近水源，设备降温
	大面积空地，数据中心的保密性
	与其他数据中心的距离，保证高速互联
	税收优惠

## 9.5 数据中心的研究热点

服务器成本
	服务器占据总成本45%，但实际利用效率上比较低（每个服务器有自己的CPU、内存等，但分配到各服务器应用不能完全利用，同时无法做到按需分配）

网络设备成本
	占成本15%，交换机、路由器、负载均衡设备，中心内部和数据中心之间的连接。
	传统属性结构的容错性不理想，设计数据中心的网络结构。

能源成本
	占成本15%，降温系统、关键设备负载、电能转化损失、照明。
	硬件系统的革新，电脑的高性能模式和节电模式。
	设置更高的工作环境温度，减少降温系统的工作时间。

## 9.6 数据中心与云存储

最早亚马逊提供计算资源租赁服务，弹性计算云（提供海量数据计算服务）和简单存储服务（可伸缩、可靠、高可用、低成本的存储服务）。
