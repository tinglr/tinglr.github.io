---
layout: page
title: 项目
comments: true
permalink: /projects/
---

* content
{:toc}

# - While Group工作室 #

[https://tinglr.github.io](https://tinglr.github.io/)
  

![WhileGroup]({{ site.url }}/static/img/WhileGroup_small.png)


<img width="80" height="80" src="{{ site.url }}/static/img/WhileGroup_small.png"/>

<br>

###  **- 简介**

**简单，艺术，激情**<br>
**Life feeds on negative entropy**<br>

资源整合，分布式协作，移动办公，自由创造，自由连接。<br>

庶務：每月开一次分享会 输入 输出<br>
庶務：每周登陆一次团队打卡连续<br>
连续一直<br>


<br>


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

<br>


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



<br>

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


<br>




 








<br>




----------