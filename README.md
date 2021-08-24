# HP-ZHAN-66-Pro-14-G3-OC-EFI
现在的黑苹果已经比较成熟了，记得当时14年折腾过半个月，太痛苦放弃了，现在从过，新人从零开始搞的，也从clover到opencore 方式，过程中感谢爬过的远景、黑果小兵blog、黑苹果社区等等。

# 更新日历：

#### ·2021-08-24 OC版本更新至0.7.2，MacOS 版本实测在线从11.5-->11.5.1-->11.5.2 ,正常使用中

#### ·2021-07-02 OC版本更新至0.7.0

#### ·2021-06-30 Bigsur11.0-11.4 仍有模拟15-16寸机型，会有外接显示器无效的问题（只实测过HDMI），13寸MBP、27村的iMac、Macmini 都试过，是没问题的。

#### ·2021-06-29 重新安装BigSur11.4，过程中发现： 笔记本电池的驱动方法是：（ SMCBatteryManager.kext + ECEnabler.kext ）
要多留意文章：https://github.com/daliansky/OC-little

#### ·2021-06-22 更换了SN550，全盘新装10.15.7 ，使用了几天，转彩虹现象确实消失了。。花钱买不遭罪啊

#### ·2021-06-18 连续用一段时间后，在操作ppt之类的时候，会莫名奇妙的的出现转彩虹的现象（卡顿），网上查了基本都说是因为PM981 硬盘的事，所以趁着618，赶紧下单买了个西数SN550 的盘。准备重装看下还有没有这个问题

#### ·2021-06-10 重新安装macos 后，问题依旧，上述方法也无法解决，泪崩中~~

# 注意事项：
####  1. OS 安装方式是用Paragon Software/Hard Disk Manager 17 Advanced 硬盘恢复方式进行的（注意一定要有这两个文件 SSDT-NVMe.aml（这个可能需要调整） HackrNVMeFamily.kext，否则硬盘恢复后也是进不去会报错）

####  2. HDMI 投影 折腾我将近3周， 一直在不断尝试新的显卡驱动和补丁，最终的关键点： HDMI的通道值一定要比内屏通道值隔几个数字（比如我的内屏通道是 8，HDMI的通道值是12，此前一直默认9，就出现投影HDMI后，内屏黑屏，外接显示器是正常的问题）

#### 3. Bigsur11.0-11.4  启动进入恢复模式无效存在问题，关闭SIP，只能通过OC配置进行了：

​    OC引导，使用OC的配置工具，也是打开config.plist

​	找到NVRAM，中间部分找到并选中 7C436110-AB2A-4BBB-A880-FE41995C9F82

​	在右边部分空白处，新建csr-active-config ，DATA类型

​	10.15 的系统值写入 E7030000

​	11的系统值写 77000000

## 因我第一次自己创建github，有些内容还不会，如要下载，下载后请处理：
        1. 文件夹内如有.DS_Store 这个文件，可以删除。。 
   我只是想分享自己的记录，顺便共享给同样型号想要折腾的同学，如有问题，请不要人身攻击，网络暴力受不了～～


# 特别感谢：

   TKS @gxzzzzzzzzz  ：https://github.com/gxzzzzzzzzz/HP_zhan66_pro_14_g3     

   TKS @xiaoshimu ：https://github.com/xiaoshimu/macos-opencore-hp-zhan66-pro15-g3-i7-10510u
    
   最终我是基于xiaoshimu 大佬的文件，做的调整。

# ----------电脑配置---------------
  电脑型号：            HP ZHAN 66 Pro 14 G3 笔记本电脑

  处理器：              英特尔 Core i7-10510U @ 1.80GHz 四核

  主板：                惠普 86A5 ( I/O - 0284 for Intel 400 Series 芯片组 Family On-Package Platform Controller Hub )

  显卡：                Nvidia GeForce MX250 ( 2 GB )

  内存：                16 GB ( 三星 / 镁光 )

  ~~主硬盘：              三星 MZVLB512HBJQ-000H1 ( 512 GB / 固态硬盘 )（没错，就是传说中的981 无解盘）~~

  主硬盘：              **西数 WDC WDS500G2B0C-00PXH0 ( 512 GB / 固态硬盘 )**

  数据盘：              **希捷 ST1000LM048-2E7172 ( 1024 GB / SATA硬盘 )**

  显示器：              LG LGD0619 ( 14 英寸  )

  声卡：                英特尔 英特尔智音技术音频控制器

  网卡：                英特尔 Wireless-AC 9462

  # OS版本：            10.15.6 


#  -------最终效果-----

  CPU：已睿频

  显卡：仿冒UHD630

  网卡：有线网卡

  WI-FI：ok（除有个别网络路由经常性断开重连）

  触摸板：HID支持

  电池显示：可以

  显示器亮度：可以

  蓝牙： 已支持

  SD卡：已支持

  USB：已修复

  声卡：OK

  HDMI投影：OK

显卡：Nvidia GeForce MX250 已屏蔽

指纹：不支持。

