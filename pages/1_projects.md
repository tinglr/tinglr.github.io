---
layout: page
title: Projects
comments: true
permalink: /projects/
---

* content
{:toc}

# - While Group工作室 #

[https://tinglr.github.io](https://tinglr.github.io/)
  
![While Group](static\img\WhileGroup_small.png)  



<img width="80" height="80" src="static/img/WhileGroup_small.png"/>

<br><br><br><br><br><br><br><br><br><br><br>

###  **- 简介**

**简单，艺术，激情**<br>
**Life feeds on negative entropy**<br>

资源整合，分布式协作，移动办公，自由创造，自由连接。<br>

庶務：每月开一次分享会 输入 输出<br>
庶務：每周登陆一次团队打卡连续<br>
连续一直<br>


<br><br><br><br><br><br><br><br><br><br><br>


###  **- 成员**

#### **成员1**

tinglr<br>
坐标：深圳<br>
工作职位：电子工程师<br>
工作经验：5年<br>


##### **参与的项目：**<br>
（作为项目成员参与产品立项到量产全过程，分担项目部分设计工作）<br>
   * 项目1.WiFi智能插座
   * 项目2.CO一氧化碳报警器
   * 项目3.(65W)PD/QC快充
   
#### **主创的项目：**
（从立项到量产，承担主要软硬件设计工作）<br>
   * 项目1.红外转发器
   * 项目2.MODBUS主机/网关
   * 项目3.HVAC温控器

#### **主要输出能力：**

<br><br><br><br><br><br><br><br><br><br><br>


----------


# 嵌入式linux相关 #

<br><br><br>

###  **- linux指令操作**

**1.复制hello命令到某文件夹**<br>
cp hello /home/root/<br>
cp -r dir1 dir2 表示将dir1及其dir1下所包含的文件复制到dir2下

**2.解压命令**<br>
tar -xvf filename.tar.gz<br>
tar -xvf filename.tar.bz2<br>
tar -xvf filename.tar.xz<br>
tar -xvf filename.tar.Z<br>

**3.普通编译**<br>
gcc -o lcd_test lcd_test.c

**4.交叉编译命令**<br>
arm-linux-gnueabihf-gcc -o lcd_test lcd_test.c

**5.加入数学库后**<br>
arm-linux-gnueabihf-gcc -o eye eye.c -lm //eg：sqrt未定义的引用

**6.挂载tf卡**<br>
df -h

**7.杀死进程**<br>
kill 559
  
**8.使用 rm -rf test 强制删除test文件夹**<br>
-r 强制删除
-f 忽略提示
  
**9.查询Ubuntu位数**<br>
getconf LONG_BIT



<br><br><br><br><br><br><br><br><br><br><br>

### **操作imx6ul的一些记录**

1.修改启动程序<br>

```c
python /usr/share/myir/init_boardcfg.py &

if test -z "$DBUS_SESSION_BUS_ADDRESS" ; then
   eval `dbus-launch --sh-syntax`
   echo "D-Bus per-session daemon address is: $DBUS_SESSION_BUS_ADDRESS"
fi
export DBUS_SESSION_BUS_ADDRESS="$DBUS_SESSION_BUS_ADDRESS"

/home/myir/mxbackend &
/home/myir/mxapp --platform linuxfb &
python /usr/share/myir/www/server.py &
 
```

 
 2.库的链接关系查询<br>
```c
root@ubuntu:/usr/local/arm/arm-2009q3/arm-none-linux-gnueabi/libc/lib# file libfreetype.so
libfreetype.so: symbolic link to `libfreetype.so.6.9.0'
file libfreetype.so
libfreetype.so: symbolic link to `libfreetype.so.6.9.0'
```

3.使用freetype<br>
```c
tar xvf freetype-2.4.10.tar.bz2     //解压
./configure --host=arm-linux-gnueabihf     //配置为ARM-Linux
make
make DESTDIR=$PWD/tmp install      //安装到一个临时目录，再把里面的头文件拷贝到我们的交叉编译工具链里面去
  
/usr/local/arm/gcc-linaro-4.9.4-2017.01-x86_64_arm-linux-gnueabihf/arm-linux-gnueabihf/libc/lib#
/usr/local/arm/gcc-linaro-4.9.4-2017.01-x86_64_arm-linux-gnueabihf/arm-linux-gnueabihf/libc/usr/include#
cp * /usr/local/arm/gcc-linaro-4.9.4-2017.01-x86_64_arm-linux-gnueabihf/arm-linux-gnueabihf/libc/lib -d -rf
cp *so* /home/c/aaa/show_file_ask/lib/ -d

cp * /usr/local/arm/gcc-linaro-4.9.4-2017.01-x86_64_arm-linux-gnueabihf/arm-linux-gnueabihf/libc/usr/include -rf
cd /usr/local/arm_linux_4.2/arm-none-linux-gnueabi/include
mv freetype2/freetype .
```
  
4.使用tslib<br>
```c
 tar -xvf tslib-1.4.tar.bz2

 
   # cd tslib
   # ./autogen.sh
   echo "ac_cv_func_malloc_0_nonnull=yes">arm-linux-gnueabihf.cache 
   # ./configure --host=arm-linux-gnueabihf --cache-file=arm-linux-gnueabihf.cache --enable-inputapi=no -prefix=/usr/local/tslib 
   # make
   # make install
```

```c
   imx6ul:
	char: 1
	short: 2
	int: 4
	long: 4
	float: 4
	double: 8

  ubuntu16.04 
	char:1
	short:2
	int:4
	long:8
	float:4
	double:8
```


<br><br><br><br><br><br><br><br><br><br><br>



  
4、表格 （建议在表格前空一行，否则可能影响表格无法显示）
 
 表头  | 表头  | 表头
 ---- | ----- | ------  
 单元格内容  | 单元格内容 | 单元格内容 
 单元格内容  | 单元格内容 | 单元格内容  
 








<br><br><br><br><br><br><br><br><br><br><br>



----------
# - 网站导航

常用网站：<br>
[新加坡网站](http://14.29.226.209:81/)<br>
[Github](https://github.com/)<br>
[Python库](https://www.lfd.uci.edu/~gohlke/pythonlibs/)<br>
[搜狗翻译](https://fanyi.sogou.com/)<br>
[拷贝兔](https://cp.anyknew.com/)<br>
[在线实用工具集合PDF转HTML](https://www.toolnb.com/)<br>


有趣网站：<br>
[大学资源网：http://www.dxzy163.com/](http://www.dxzy163.com/)<br>
[简答题：http://www.jiandati.com/](http://www.jiandati.com/)<br>
[必看网（人生必看的书籍）：https://www.biikan.com/](https://www.biikan.com/)<br>
[查无此人（刷新网站，展现一张AI 生成的人脸照片](https://thispersondoesnotexist.com/)<br>
[术语在线：http://www.termonline.cn/](http://www.termonline.cn/)<br>


资源搜索  
[DogeDoge搜索引擎](http://www.dogedoge.com)<br>
[视频资源下载爱扒](https://www.zyboe.com/)<br>
[电影天堂https://www.dy2018.com/](https://www.dy2018.com/)<br>
[奶牛快传](https://www.cowtransfer.com)<br>
[文叔叔（大文件传输，不限速）](https://www.wenshushu.cn/)<br>
[香当网（年终总结，个人简历，事迹材料，租赁合同，演讲稿）](https://www.xiangdang.net/)<br>
[二维码生成](https://cli.im/)<br>
[码力全开（UI的资源库）](https://www.maliquankai.com/designnav/)<br>
[图片无限变放大](http://bigjpg.com/zh)<br>
[小森林导航](http://www.xsldh6.com/)<br>

[找免费字体](http://www.hellofont.cn/)<br>
[查字体是否可以商用网站](https://fonts.safe.360.cn/)<br>
[爱给网（免费下载音效视频）](http://www.aigei.com/)<br>
[在线视频剪辑](https://bilibili.clipchamp.com/editor)<br>




阿木影视：https://www.aosk.online/   
电影推荐（分类别致）：http://www.mvcat.com  
APP影院：https://app.movie

去看TV：https://www.qukantv.net/

动漫视频网：http://www.zzzfun.com/

94神马电影网：http://www.9rmb.com/

NO视频官网：http://www.novipnoad.com/

蓝光画质电影：http://www.languang.co/

在线看剧：http://dy.27234.cn/

大数据导航：http://hao.199it.com/

多功能图片网站：

https://www.logosc.cn/so/

牛牛TV：http://www.ziliao6.com/tv/

VideoFk解析视频：

http://www.videofk.com/

蓝调网站：http://lcoc.top/vip2.3/

永久资源采集网：

http://www.yongjiuzy1.com/





学设计 


免费音频素材：https://icons8.cn/music

新CG儿（视频素材模板，无水印+免费下载）：

https://www.newcger.com/

Iconfont（阿里巴巴矢量图标库）：

https://www.iconfont.cn/

小图标下载：https://www.easyicon.net/

Flight Icon：https://www.flighticon.co/

第一字体转换器：http://www.diyiziti.com/

doyoudosh（平面设计）：

www.doyoudo.com

企业宣传视频在线制作：https://duomu.tv/

MAKE海报设计官网：http://maka.im/



搞文档

即书（在线制作PPT）：

https://www.keysuper.com/

PDF处理：https://smallpdf.com/cn

PDF处理：https://www.ilovepdf.com/zh-cn

PDF处理：https://www.pdfpai.com/

PDF处理：https://www.hipdf.cn/

图片压缩，PDF处理：

https://docsmall.com/

腾讯文档（在线协作编辑和管理文档）：

docs.qq.com

ProcessOn（在线协作制作结构图）：

www.processon.com

iLovePDF（在线转换PDF利器）：

www.ilovepdf.com

PPT在线制作：https://www.woodo.cn/

PDF24工具（pdf处理工具）：

https://tools.pdf24.org/en

IMGBOT（在线图片处理）：

www.imgbot.ai

福昕云编辑（在线编辑PDF）：

edit.foxitcloud.cn

TinyPNG（在线压缩图片）：tinypng.com



优品PPT（模板下载）：

http://www.ypppt.com/

第一PPT（模板下载）：

http://www.1ppt.com/xiazai/

三顿PPT导航：sandunppt.com




找图片

电脑壁纸：http://lcoc.top/bizhi/

https://unsplash.com/

https://pixabay.com/

https://www.pexels.com/

https://visualhunt.com/

https://www.ssyer.com/

彼岸图网：http://pic.netbian.com/

极像素（超高清大图）：

https://www.sigoo.com/

免费版权图片搜索：

https://www.logosc.cn/so/


<br><br><br><br><br><br><br><br><br><br><br>


----------

