## 第0章 计算器概论  
### 0.1 计算机：辅助人脑的好工具  
所谓的计算机，实际上是都是一种计算器，计算器其实是：接受用户输入的指令和数据，经由中央处理器的数学与逻辑单元运算处理后，以产生或储存成有用的信息。  
#### 0.1.1 计算机硬件的五大单元  
输入单元、输出单元、CPU内部的控制单元、算数逻辑单元、主存储器  
#### 0.1.2 一切设计的起点：CPU的架构  
我们所使用的软件都要经过CPU内部的微指令集来达成才行。指令集的设计主要又被分为两种设计理念，即现在世界上常见到的两种主要的CPU架构。分别是精简指令集（RISC）和复杂指令集（CISC）系统。  
精简指令集（Reduced Instruction Set Computer）  
微指令集较为精简，每个指令的运行时间都很短，完成的动作也很单纯，指令的执行效能较佳；但是若要做复杂的事情，就要由多个指令来完成。  
复杂指令集（Complex Instruction Set Computer）  
微指令集的每个小指令可以执行一些较低阶的硬件操作，指令数目多而且复杂，每条指令的长度并不相同。因为指令执行较为复杂，所以每条指令花费的时间较长，但是每条指令可以处理的工作较为丰富 。  
#### 0.1.3 其他单元的设备  
系统单元  
系统单元包括CPU与内存及主板相关组件。  
记忆单元  
包括主存储器与辅助内存。  
输入、输出单元  
触摸屏、键盘、鼠标、屏幕、打印机。  
#### 0.1.4 运作流程  
#### 0.1.5 计算机用途的分类  
按照计算机的复杂度与运算能力分类：  
超级计算机（Super Computer）  
超级计算机是运作速度最快的计算机，但是维护、操作费用也最高。主要用于需要有告诉计算的计划中，如国防军事、太空科技等领域。  
大型计算机（Mainframe Computer）  
大型计算机通常也具有数个高速的CPU，可用来处理大量资料与复杂的运算。  
迷你计算机（Mini Computer）  
迷你计算机保有大型计算机同时支持多用户的特性，但是主机可以放在一般作业场所。  
工作站（Work Station）  
是针对特殊用途而设计的计算机。  
微电脑（Micro Computer）  
个人计算机。  
#### 0.1.6 计算机上面常用的计算单位（容量、速度等）  
计算机的运算能力除了CPU微指令集设计的优劣之外，主要还是由速度来决定的。同时存放在计算机存储设备当中的数据容量也是有单位的。  
容量单位  
计算机对数据的判断主要依据是有没有通电来记录信息，所以理论上对于每一个记录单位而言，它只认识0和1。  
0/1这个二进制的单位，我们称之为bit，但是bit实在是太小了，所以在储存数据时每份简单的数据都会使用到8个bit的大小来记录，因此定义出byte这个单位，关系如下：  
1Byte = 8 Bit  
1M = 1024 K = 1024 * 1024 Byte
速度单位  
CPU 的指令周期常使用MHz或者是GHz之类的单位，这个Hz其实就是秒分之一。  
在网络传输方面，由于网络使用的是bit为单位，因此网络常使用Mbps（Mbits per second）  
### 0.2 个人计算机架构及相关设备组件  
#### 0.2.1 执行脑袋运算与判断的CPU  
CPU负责大量运算，所以在CPU旁边会有一个风扇来主动散热。  
多核心则是在一个CPU封装当中嵌入两个以上的运算核心。简单来说，就是一个实体CPU外壳中，含有两个以上的CPU单元即可称之为多核心CPU了。  
频率是CPU每秒钟可以进行的工作次数。  
##### CPU的工作频率：外频和倍频  
CPU的架构主要透过北桥来链接系统最重要的CPU、主存储器与现实适配器装置。所有的设备都得掉透过北桥来连接，因此每个设备的工作频率应该要相同。于是就有了所谓的前端总线（FSB）的产生。但是因为CPU的指令周期比其他的设备都要来的快，又为了满足FSB的频率，因此厂商就在CPU内部再进行加速，于是就有所谓的外频和倍频了。  
外频：指的是CPU与外部组件进行数据传输时的速度；  
倍频：则是CPU内部用来加速工作效能的一个倍数；  
外频 * 倍频 = CPU的频率速度  
##### 32位与64位的CPU与总线【宽度】  
CPU的各项数据通通来自于主存储器，因此，如果主存储器能提供给CPU的数据量越大的话，整体系统的效能应该也会更快。这个时候就需要CPU内的内存控制芯片与主存储器间的传输速度（FSB）来说明了。  
##### CPU等级  
目前64位CPU则统称为x86_64等级。  
##### 超线程（Hyper-Threading，HT）  
现在的CPU至少都是两个核心以上的多核心CPU了，但是Intel有个很奇怪的东西，叫做CPU的超线程。  
在每一个CPU的内部将重要的缓存器分成两群，让程序分别使用这两群缓存器。  
#### 0.2.2 内存  
个人计算机的主存储器主要组件为动态随机存取内存。随机存取内存只有在通电时才能记录和使用，断电后数据就消失了，所以我们称这种RAM为挥发性内存  
##### 多通道设计  
所有的数据都必须存放在主存储器，所以主存储器的数据宽度当然是越宽越好。  
##### DRAM和SRAM  
除了主存储器之外，在个人计算机中还有许许多多的内存存在。  
CPU内的第二层高速缓存。  
##### 只读存储器（ROM）  
ROM是一种非挥发性的内存。  
BIOS是一套程序，这套程序是写死到主板上面的一个内存芯片中，也就是ROM。  
#### 0.2.3 显示适配器  
显示适配器内存容量将会影响到你的屏幕分辨率与颜色深度  
#### 0.2.4 硬盘与储存设备  
计算机系统上面的储存设备有：硬盘、软皮、MO、CD、DVD、磁带机、随身碟(闪存)、蓝光光驱。  
##### 硬盘的物理组成  
硬盘其实是由圆形磁盘盘、机械手臂、磁盘读取头与主轴马达所组成的。  
##### 磁盘盘上的数据  
数据读写是通过圆圈转圈的方式来实现的。  
磁盘的最小物理单位为扇区，同一个同心圆的扇区组合成的圆就是所谓的磁道，所有磁盘盘上面的同一个磁道可以组合成所谓的磁柱。  
##### 传输界面  
* SATA界面  
* SAS界面  
* USB界面  

##### 固态硬盘  
传统硬盘的致命问题是需要驱动马达去转动磁盘盘~这会造成严重的磁盘读取延迟。  
##### 选购与运转须知  
#### 0.2.5 扩充卡与界面  
#### 0.2.6 主板  
#### 0.2.7 电源供应器  
#### 0.2.8 选购须知  
### 0.3 数据表示方式  
计算机常用的数据是二进制的。在本节我们来谈谈数值与文字编码系统。  
#### 0.3.1 数字系统  
早期的计算机使用的是利用通电与否的特性的真空管，如果通电就是1，没有通电就是0。我们称这种只有0/1的环境未二进制制，英文为binary。  
#### 0.3.2 文字编码系统  
常用的英文编码表为ASCII系统。  
### 0.4 软件程序运作  
计算机系统将软件分为两大类，一个是系统软件，一个是应用程序。  
#### 0.4.1 机器程序与编译程序  
计算机只认识0和1，而且计算机最重要的运算与逻辑判断都是在CPU内部，而CPU是具有微指令集的。所以，当我们需要CPU帮忙工作时，就得要参考微指令集的内容，然后撰写让CPU读的懂的脚本给CPU执行，这样才能让CPU运作。  
上述流程中麻烦的几个地方：  
需要了解机器语言；  
需要了解所有硬件的相关功能函数；  
程序不具有可移植性；  
程序具有专一性；  
为了解决在上述过程中遇到的问题，计算机科学家们设计出一种让人类看得懂的程序语言，然后创造一种编译程序来将这些人类编写的程序语言转译成机器能看得懂的机器码。  
#### 0.4.2 操作系统  
操作系统，可以驱动所有的硬件，并且提供一个发展软件的参考接口出来给工程师开发软件。  
##### 操作系统核心（Kernel）  
操作系统（OS），其实也是一组程序，这组程序的重点在于管理计算机的所有活动以及驱动系统中的所有硬件。  
##### 系统呼叫（System Call）  
为了保护核心，并且让程序设计师比较容易开发软件，因此操作系统除了核心程序之外，通常还会提供一整组开发接口，那就是呼叫系统层。  
##### 核心功能  
核心功能主要是负责整个计算机系统相关的资源分配与管理，核心功能主要如下：  
系统呼叫接口（System call interface）  
程序管理（Process control）  
内存管理（Memory management）  
文件系统管理（Filesystem management）  
装置的驱动（Device drivers）  
##### 操作系统与驱动程序  
驱动程序是操作系统里面相当重要的一环。  
#### 0.4.3 应用程序  
应用程序是参考操作系统提供的开发接口所开发出来的软件，这些软件可以让用户操作，以达到某些计算机的功能利用。  
## 第一章 Linux是什么与如何学习  
Linux是在计算机上面运作的，是一组软件。  
### 1.1 Linux是什么  
#### 1.1.1 Linux是什么？操作系统or应用程序  
Linux是一套操作系统。Linux提供了一个完整的操作系统当中最底层的硬件控制与资源管理的完整架构，这个架构是沿袭Unix良好的传统来的，所以相当的稳定而且功能强大。  
### 1.3 Linux当前应用的角色  
#### 1.3.1 企业环境的利用  
网络服务器  
关键任务的应用  
学术机构的高效能运算任务  
#### 1.3.2 个人环境的使用  
桌面计算机  
手持系统（PDA、手机）  
嵌入式系统  
#### 1.3.3 云端应用  
云程序  
端设备  
### 1.4 Linux该如何学习  
#### 1.4.1 从头学习Linux基础  
不论学习什么系统，从头学起是很重要的。建议按照如下的方面进行学习：  
1.计算器概论与硬件相关知识；  
2.先从Linux的安装与指令学起；  
3.Linux操作系统的基础技能；  
4.Vim文本编辑器；  
5.Shell与Shell Script；  
6.软件管理；  
7.网络基础的建立；  
8.网络基础；  
#### 1.4.3 实战演练  
## 第二章 主机规划与磁盘分区  
## 第三章 安装CentOS 7.x  
## 第四章 首次登入与在线求助  
## 第五章 Linux的文件权限与目录配置  
Linux最优秀的地方之一就在于它的多人多任务环境。为了让各个使用者具有较保密的文件数据，文件的权限管理就很重要了。  
### 5.1 使用者与群组  
1.文件拥有者  
2.群组概念  
群组最有用的功能之一，就是当你在团队开发资源的时候了。每个账号都可以有多个群组的支持。  
3.其他人的概念  

在Linux里面，任何一个文件都具有【User、Group、Others】三种身份的个别权限。  
root用户是Linux系统的超级管理员，具有所有文件的所有权限。  
#### 5.1.1 Linux用户身份与群组记录的文件  
/etc/passwd: 记录系统上的账号与一般身份使用者；  
/etc/shadow: 记录个人密码；  
/etc/group: 记录组名；  
### 5.2 Linux文件权限概念  
#### 5.2.1 Linux文件属性  
ls--【list】：  
显示文件的文件名与相关属性；
al：  
列出所有的文件详细的权限和属性（包含隐藏文件）  
PS:隐藏文件即是文件名格式为.*的文件  
ls -al(从左到右依次展示内容为)  
权限 连结 拥有者 群组 文件容量 修改日期 文件名    
权限：共有十个字符（示例：drwxr-xr-x+），由左至右释义如下  
第一个字符代表这个文件是【目录、文件或链接文件等等】；  
接下来，三个字符一组均为【rwx】的三个参数的组合，第一组为文件拥有者可具备的权限，第二组为加入此群组之账号的权限；第三组为非本人且没有加入本群组之其他账号的权限；  
连结：记录他的权限和属性到文件系统的i-node中；  
拥有者：表示这个文件的拥有者；  
所属群组：表示这个文件的所属群组；  
文件容量：表示这个文件的容量大小，默然单位为bytes；  
修改日期：表示文件的建档日期或最近的修改日期；  
文件名：表示文档的名字；  
* Linux文件权限的重要性  
系统保护的功能；  
团队开发软件或数据共享的功能；  
未将权限设定妥当的危害；  
#### 5.2.2 如何改变文件属性与权限  
改变所属群组，chgrp  
改变文件拥有者，chown  
改变文件权限，chmod  
数字类型改变文件权限  
Linux文件的基本全新有9个，分别是owner/group/others三种身份各有自己的read/write/execute权限；  
ow
## 第六章 Linux文件与目录管理  
## 第七章 Linux磁盘与文件系统管理  
## 第八章 文件与文件系统的压缩、打包与备份  
## 第九章 Vim程序编辑器  
## 第十章 认识与学习BASH  
## 第十一章 正规表示法与文件格式化处理  
## 第十二章 学习Shell Scripts  
## 第十三章 Linux账号管理与ACL权限设定  
## 第十四章 磁盘配额（Quota）与进阶文件系统管理  
## 第十五章 例行性工作排程（crontab）   
## 第十六章 进程管理与SELinux  
## 第十七章 认识系统服务（daemons）
## 第十八章 认识与分析登录档  
## 第十九章 开机流程、模块管理与Loader  
## 第二十章 基础系统设定与备份策略  
## 第二十一章 软件安装：原始码与Tarball  
## 第二十二章 软件安装RPM、SRPM与YUM  
## 第二十三章 XWindows设定介绍  
## 第二十四章 Linux核心编译与管理



