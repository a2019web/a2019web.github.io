---
date: 2013-12-23 06:11:13+00:00
title: Google出品的自动Web安全扫描程序 Skipfish 安装
categories:
- web安全
---

Skipfish是由google出品的一款自动化的网络安全扫描工具，该工具可以安装在linux、freebsd、MacOS X系统和windows(cygwin)。   
谷歌工程师Michal Zalewski称，尽管Skipfish与Nikto和Nessus等其他开源扫描工具有相似的功能，但Skipfish还具备一些独特的优点。 Skipfish通过HTTP协议处理且占用较低的CPU资源，因此它的运行速度比较快。Skipfish每秒钟可以轻松处理2000个请求。   
  
Skipfish-2.09b更新日志：   
修正了一些可能触发程序崩溃的bug   
检测到的问题报告可以存储到json文件里面   
新增mod_status, mod_info, MySQL dump, phpMyAdmin SQL dump和robots.txt签名   
新增Flash和Silverlight跨域策略签名   
  
  
  
**需要的依赖：**



    
    <code>sudo apt-get install libpcre3-dev  libidn11-dev openssl-devel gcc libidn-devel</code>


**  
**先安装http://ftp.gnu.org/gnu/libidn/libidn-1.18.tar.gz   
./configure   
make   
make install   
  
**完成后**   
wget http://code.google.com/p/skipfish/downloads/detail?name=skipfish-2.09b.tgz   
直接make&&make install   
需要openssl和openssl-devel   
  
安装完成后，进入skipfish-2.09b目录，cp dictionaries/completes.wl skipfish.wl   
运行：   
./skipfish -o /root/scan.txt http://www.baidu.net or

./skipfish -o output_folde http://www.baidu.com

//其中output_folder是输出目录，扫描结束后可打开index.html查看扫描结果  
  
官方地址：[http://code.google.com/p/skipfish/](http://code.google.com/p/skipfish/)
