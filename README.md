# Planck-Pi-IoT
复刻稚晖君的Planck-Pi的一些注意事项和说明。

推荐复刻群号如下：

**287810522**


![287810522](/Images/287810522.jpg)

## 前言

复刻Planck-Pi初衷，本人之前对这个小开发板的使用场景没想好，所以一直没有着手复刻，然后最近想到可以拿这个小东西学习嵌入式开发的一些知识，就想复刻一个拿来学习了，刚好社区也有一些人进行了分享，外加这个主控芯片的社区也有一些其他的开发板，所以资料也挺全的就拿来复刻学习了。

**成品焊接实物图**

![zhengmian-ok](/Images/zhengmian-ok.jpg)

![fanmian-ok](/Images/fanmian-ok.jpg)



## 物料准备和硬件焊接

### 1. PCB板子的打板流程

首先将稚晖君的项目仓库内容克隆到本地，不会使用的git的可以直接下载压缩文件。

**项目地址如下：**

https://github.com/peng-zhihui/Planck-Pi

命令行执行下面的指令获取文件。

```
git clone https://github.com/peng-zhihui/Planck-Pi.git
```

![code-clone](/Images/code-clone.png)

项目内容下载到本地以后就可以将pcb打板的文件打包，然后提给嘉立创平台只做PCB，温馨提示由于项目是四层板子，不免费的话价格在40元可以打到6个板子。

![gerber](/Images/geber-imag.png)

首先访问嘉立创网站进行PCB打板，这个大家应该可以了解嘉立创这个公司主营业务。

网站地址：https://www.jlc.com

![网站图片](/Images/jlc-home.png)

小白需要弄明白PCB和SMT的区别。

+ PCB就是电路板的制作

+ SMT的话就是把电路板和元器件都给焊接好

我们只是打板只需要注册进入下单平台，建议大家使用下单助手下单，因为会很便宜，文档我就使用网页版进行演示了，大致的流程是。

1. 进入后台 => 2. 进入PCB下单板块 => 上传Gerber文件 => 调整参数 => 然后下单

涉及到的图片如下：

**后台页面**

![order-info](/Images/smt-pcb.png)

**PCB上传页面**
![gerber-up](/Images/gerber-up.png)

**订单配置页**
![order-page](/Images/order-page.png)

**参数配置页面**

+ 板材类别选择FR-4
+ 确认生产稿可以不管（板子已验证）
+ 层压顺序选择文件中已有

像钢网 smt都不用勾选，其他的默认就行，配置到发票抬头，然后写好地址就可以下单了，不要担心有问题，有问题客服就会打电话了。

**重要的问题是选择颜色是要加钱的，所以绿色最便宜**

![order-data](/Images/order-data.png)

收到快递以后的成品就如下图所示了，板子很小的。

![zhengmian-empty](/Images/zhengmian-empty.jpg)

![fanmian-empty](/Images/fanmian-empty.jpg)


### 2. 物料购买

主要的元器件我分别在立创商城买了一部分电容电阻，然后在优信电子买了一些电路的外设，不过我由于没看仔细，多买了肖极特二极管和led灯。

仓库的立创商城购物车详情可以直接导入到立创商城的购物车，大家就可以对着下单了，我的数量有的会多选一个你们可以对着稚晖君仓库的物料表自己添加数量。

立创商城地址：https://www.szlcsc.com/

选择bom上传

![bom-data](/Images/bom-data.png)

**立创商城的送货单如下：**

![jlc-bom](/Images/lichuang.png)

**优信电子的物料：**
![youxin1](/Images/YOUXIN1.png)
![youxin2](/Images/YOUXIN2.png)

**主控及其他的物料**
![zhukong](/Images/F1C200S-PAM8301AAF.png)
![jingzhen](/Images/jingzhen-24MHZ.png)

**主要物料的淘宝地址如下：直达**

| 值                                                           | 封装                       | 数量 | 分类     |                         备注                          |
| ------------------------------------------------------------ | -------------------------- | ---- | -------- | :---------------------------------------------------: |
| [F1C200S](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.2c122e8dDNOo2F&id=629042296049&_u=eqc0n0pd66f)                                                       | QFN-88                   | 1    | 主控芯片 |淘宝购买               |
| [PAM8301AAF](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.2c122e8dDNOo2F&id=594879585876&_u=eqc0n0p1034)                                                       | SOT23-6                   | 1    | 音频放大器 |丝印FPA**              |
| [USB A母 AF](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.2c122e8dDNOo2F&id=575668586035&_u=eqc0n0pe632)                                                       |                    | 1    | USB A母 AF |短体10.0 MM 厚6.3 MM 6.8全贴片无边              |
| [TF卡座](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.2c122e8dDNOo2F&id=522573245737&_u=eqc0n0p42f9)                                                       |                    | 1    | micro sd卡座 |
| [3*4 龟仔/微动/轻触开关](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.2c122e8dDNOo2F&id=546724645617&_u=eqc0n0pf35d)                                                       |                    | 1    | 3*4 龟仔/微动/轻触开关 |
| [0.78寸OLED裸屏显示液晶屏](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.2c122e8dDNOo2F&id=665034068875&_u=eqc0n0p72a0)                                                       |                    | 1    | 显示屏 |分辨率128*80 SPI接口 SH1107驱动              |
| [24MHz](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.1f3c2e8df9Af9i&id=569633363622&_u=b20q7cgb7b7b) | 晶振-3P                    | 1    | 晶振     |   

### 3. 焊接的注意事项

我是参考攻城狮星河文档焊接的

[手把手教你制作一块Linux开发板(基于Planck-pi)](https://blog.csdn.net/qq_43257914/article/details/125353029)

**焊接流程如下：**

先焊接电源部分 => 确保电源测试点电压ok => 进行串口芯片焊接 => 然后就是其余的电容电阻元器件的焊接 => 焊接主控 => 最后再焊接屏幕和排针

先抛出注意事项

#### 3.1 8301注意硬件顺序
这个芯片的问题点在于它本身不能从焊接图上看出方向，所以需要根据芯片手册和电路图确认方向。但是大家打开电路图不方便的话，就可以看这个文档了，芯片手册如图。

**芯片手册图**
![8301-fangxiang](/Images/8301-doc.png)

**电路图方向**
![8301-pcb](/Images/8301-pcb.png)

两张图结合就会发现其实芯片上的字母要朝下就行了，如下图所示：
![wanzheng](/Images/zhengmian-8301.jpg)


#### 3.2 电容电阻注意两边的焊锡（不然电压测试点可能会不正常）

一定要注意EA3036附近的电容电阻的两侧没有出现短路的情况，如果测试点电压不正常一定要先处理好电压再焊接主控，不然会烧坏元器件，电压不正常最简单的办法就是用焊油涂抹电容电阻两侧，然后通过风枪调到最低风速吹板子，然后用镊子轻轻的晃动，让电容电阻自动吸附，去除多余的锡以后再次上电测试测试点电压，正常以后再进行后期的焊接。
![3036](/Images/fanmian-dianyuan.jpg)

#### 3.3 贴片发光二极管正负极

贴片LED的背面一般会有一个三角形，我买的背面是一个绿色的三角形，三角形尖头指向的方向就是负极，和板子上的方向一致就可以了。
![led-img](/Images/led-img.png)
![led-pcb](/Images/led-pcb.png)

[LED的正负极区分](https://jingyan.baidu.com/article/fd8044fa07f41c5030137a60.html)

#### 3.4 系统指示灯亮 但是串口不打印数据 需要检测串口芯片焊接

如图设备的灯亮的正常，设备列表也有串口设备，但是串口打印不出数据，这个时候我们要重点检测串口设备是否虚焊，因为主控虚焊可能直接就不会亮灯。
![device-list](/Images/device-list.png)
![port-led](/Images/port-led.jpg)

这些问题解决了我们就可以真正的登录设备连接设备了，当然串口不打印数据的问题，我们可以在设备登录栏目进行测试才会遇到问题。


## 设备登陆和联网

### 1. 系统镜像下载烧录

首先我们可以先到这个网友的网站下载相关的文件作为备用。

https://www.xn--w9q392c0zw.cn/download/Planck%20Pi%20%E7%A8%9A%E6%99%96f1c200s%E8%B5%84%E6%96%99/

![docs](/Images/f1c200s-docs.png)

【PS】由于稚晖君制作的镜像可能会有问题，但是大家还需要Debian镜像，可以从本仓库的发布里下载对应的镜像文件,此镜像为复刻群管理制作，亲测可用。

![debian-img](/Images/debian-image.png)

+ balenaEtcher-Setup-1.7.9.exe 程序的安装
+ 本仓库发布镜像下载
+ 准备内存卡并用balenaEtcher烧录

![balena](/Images/balenna.png)

镜像烧录完成以后，插上板子，板子连接到电脑注意正反插，初次使用建议正插，在电脑可以识别出一个串口设备，如果串口设备需要安装驱动大家记得通过网络下载对应的驱动。

![cp210](/Images/cp210.png)

到此板子上的led也会跟着亮起来了，大家就可以通过工具登录系统了。


### 2. 相关工具准备

+ 串口终端
+ ssh工具
+ ftp工具

我采用的方式是微软开源终端程序，然后使用串口程序插件进行的串口登录和ssh连接。

串口插件地址：
[SerialPortForWindowsTerminal](https://github.com/Zhou-zhi-peng/SerialPortForWindowsTerminal)

终端配置

![terminal](/Images/terminal-port.png)

串口登录页面
![port-connect](/Images/port-connect.png)

这个镜像登录没有密码的，所以不用担心进入不了系统。

登录成功以后效果如下：

![connect-ok](/Images/connect-ok-ui.png)

由于此镜像已经把网络配置好，我们不需要特别的配置。

板子IP：192.168.137.2

### 3. 设备联网操作

上面已经通过串口成功登录设备，我们需要反插设备，然后让电脑通过usb共享网络给板子，这样板子就能连接到互联网。

参考稚晖君和其他人的操作，电脑成功安装usb-rndis驱动，网络设备会识别出如下设备。

![usb-rndis](/Images/usb-rndis.png)

在高级网络里我们可以看到多出一个设备。

![usb-network](/Images/usb-network.png)

这个时候我们可以通过ssh登录到板子，但是板子还不能联网。

连接指令：
```
ssh root@192.168.137.2
```
![ssh-connect](/Images/ssh-connect.png)

我们需要使用此刻电脑使用的网络设备进行网络共享，我目前使用的是wifi设备，可以查看网络属性，然后切换到共享菜单按图上操作。

![network-ok](/Images/network-ok.png)

设置完，板子就能正常ping百度了，效果如下。

![network-ok-ui](/Images/network-ok-ui.png)


## 基础应用环境测试

F1C200S芯片属于armv5，所以很多应用并不能直接支持，比如go语言开发环境，我在测试使用的时候找到一个国外的网友通过源码编译的二进制文件，也进行了安装测试，效果还是可以的，可以进行程序的运行。

参考文档：
[How to run ASP.NET 5 Beta 3 or GoLang on a Raspberry Pi 2](https://www.hanselman.com/blog/how-to-run-aspnet-5-beta-3-or-golang-on-a-raspberry-pi-2)

我们需要使用ftp将下载的二进制文件上传到开发板，连接配置如下图：

![ftp](/Images/ftp.png)

成功连接就可以进行文件上传解压和环境变量配置。

运行效果如下：
![run-go-on-pi](/Images/run-go-onpi.png)

## 结尾

整体复刻难度不大，但是重点需要我们耐心测试，尤其是测试点电压一定要确保是正常的，不然主控可能会烧毁。

板子很小巧很适合进行嵌入式系统移植的学习，也或者是物联网开发学习。

本人就是看中了它的引脚操作，所以想试着进行学习，目前屏幕的操作还没有人发布代码，未来我会尝试编写屏幕的代码进行屏幕的测试。

**祝大家早日拥有自己的Planck-Pi，有问题可以提问题。**
