# Planck-Pi-IoT
复刻稚晖君的Planck-Pi的一些注意事项和说明。

## 前言

复刻Planck-Pi初衷，本人之前对这个小开发板的使用场景没想好，所以一直没有着手复刻，然后最近想到可以拿这个小东西学习嵌入式开发的一些知识，就想复刻一个拿来学习了，刚好社区也有一些人进行了分享，外加这个主控芯片的社区也有一些其他的开发板，所以资料也挺全的就拿来复刻学习了。

**板子和成品焊接实物图**

![zhengmian-empty](/Images/zhengmian-empty.jpg)

![fanmian-empty](/Images/fanmian-empty.jpg)

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


### 2. 物料购买

### 3. 焊接的注意事项

| 值                                                           | 封装                       | 数量 | 分类     |                         备注                          |
| ------------------------------------------------------------ | -------------------------- | ---- | -------- | :---------------------------------------------------: |
| [F1C200S](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.2c122e8dDNOo2F&id=629042296049&_u=eqc0n0pd66f)                                                       | QFN-88                   | 1    | 主控芯片 |淘宝购买               |
| [PAM8301AAF](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.2c122e8dDNOo2F&id=594879585876&_u=eqc0n0p1034)                                                       | SOT23-6                   | 1    | 音频放大器 |丝印FPA**              |
| [USB A母 AF](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.2c122e8dDNOo2F&id=575668586035&_u=eqc0n0pe632)                                                       |                    | 1    | USB A母 AF |短体10.0 MM 厚6.3 MM 6.8全贴片无边              |
| [TF卡座](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.2c122e8dDNOo2F&id=522573245737&_u=eqc0n0p42f9)                                                       |                    | 1    | micro sd卡座 |
| [3*4 龟仔/微动/轻触开关](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.2c122e8dDNOo2F&id=546724645617&_u=eqc0n0pf35d)                                                       |                    | 1    | 3*4 龟仔/微动/轻触开关 |
| [0.78寸OLED裸屏显示液晶屏](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.2c122e8dDNOo2F&id=665034068875&_u=eqc0n0p72a0)                                                       |                    | 1    | 显示屏 |分辨率128*80 SPI接口 SH1107驱动              |
| [24MHz](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.1f3c2e8df9Af9i&id=569633363622&_u=b20q7cgb7b7b) | 晶振-3P                    | 1    | 晶振     |   


## 设备登陆和联网

## 基础应用环境测试

## 结尾
