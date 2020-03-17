# linux 的学习目标：
## 01 linux的终端命令：
###	掌握20个左右终端命令：
|command|    |meaning|
|:------:|------|------|
|ls     |list     |查看文件夹下内容|
|pwd    |print work directory|   查看当前所在文件夹|
|cd	|change directory|	切换文件夹|
|touch	|touch|	新建文件|
|mkdir	|make directory|	创建目录|
|rm	|remove|	删除文件|
|clear	|clera   |清空|
## 02.终端命令格式
###	command [-options] [parameter]  
  命令   	-选项	参数
## 03.查阅命令帮助信息：
###	command --help   
 man command	
  
#### manual
 	空格：下一页  
	回车：滚动一行  
	b：回滚一屏  
	f：前滚一屏  
	q：退出  
  
## 04.和文件目录相关的终端命令：
###  自动补全：tab键，    
 曾经使用的命令： 上下键。  
#### 隐藏文件：ls -a所有。-l 列表。  -h 大小。  
  
### 通配符的含义
|通配符|含义|
|:---:|------|
| * |代表任意个数个字符|
|?|代表任意一个字符|
|[]|表示可以匹配的字符中任意一个|
|[a-f]|从a-f中任意一个字符|
  
  
|command|meaning|
|:---:|------|
|cd|change directory|
|||
|cd+回车|切换到当前用户的主目录（/home/用户目录）|
|cd ~|同上|
|cd .|在当前目录保持不变|
|cd ..|切换到上一级文件夹|
|cd -|最近两次目录中切换|
|||
|touch|创建文件或修改以存在文件的末次修改时间|
|mkdir|创建目录或递归目录|
|mkdir -p| 创建递归目录|
|rm|remove|
|rm -r|删除目录|
|rm -f|强制删除，即使文件不存在，也不会有任何提示|
|rm -rf * |如果发生在根目录下，是世界末日|
|tree[目录名]|显示目录中的树状图,tree;tree ~|
|tree -d| 只显示目录|
|||
|cp|copy|
|cp 原文件 目标文件|cp ~/documents/readme.txt ./readme.txt 或者目标文件改成.|
|cp -i|覆盖文件前提示|
|cp -r|复制目录，|
|||
|mv|move 文件或目录,可以改名|
|mv -i|移动覆盖文件前提示|
|||
|cat|concatenate|
|cat -b|给每行编号，忽略空行|
|cat -n|给每行编号，包括空行|
|more|more,查看同man|
|grep|grep,搜索文本，grep -i "hello python" 123.txt|
|grep -n|所有包含文本的行及行号|
|grep -v|所有不包含文本的行及行号|
|grep -i|不区分大小写|
|grep ^a|行首，搜索以a开头的行|
|grep ke$|行尾，搜索以ke结尾的行|
|||
|echo|终端显示命令|
|echo >|在定向文件中显示内容 echo XXX > XX.XX|
|>|把内容覆盖到XX文件中|
|>>|把内容追加到XX文件中|
|重定向|把参数文字直接输入到一个文件中保存起来|
|>,>>|重定向|
|管道符|通过管道把第一个命令的执行结果，作为另一个命令的输入|
|||
|shutdown 选项 时间|重启、关闭系统|
|shutdown 10 或者 shutdown 20:25|关机时间设定|
|shutdown -c|取消关机|
|shutdown -r|重启|
|||
|ifconfig|configure a network interface:查看配置计算机当前的网卡配置信息|
|ping ip地址|检测目标ip地址的连接是否正常|
|||
|远程登录，远程管理|复制文件|
|ssh|secure shell|
|域名|ip地址是一组用点分割的数字，域名是ip地址的别名|
|端口号|找到服务软件|
|默认端口|ssh服务器：22；web服务器：80；HTTPS：445；FTP服务器：21|
|ssh [-p port] user@remote||
|user|远程机器上的用户名，如果不指定，默认当前用户|
|remote|远程机器的地址，可以是ip/域名，或者是别名|
|port|是SSH Server监听的端口，如果不指定，默认为22|
|-p port|是22时可以省略，否则-p 数字|
|windows下SSH客户端|putty 和 XShell|
|scp| secure copy;复制文件夹和cp一样用-r|
|scp **-P** user@ip||
|scp -P port 01.py user@remote:Desktop/01.py |把当前目录下的01.py复制到远程家目录下Desktop/01.py|
|scp -P port user@remote:Desktop/01.py 01.py|把远程家目录下的Desktop/01py文件复制到本地当前目录下的01.py|
|scp -P 22 python@172.16.140.138:Desktop/01.py .01.py|scp -P 22 -r python@172.16.140.138:Desktop/01.py .01.py|
|windows中|用FileZilla传输,端口写21，因为是ftp服务器|
|||
|**SSH高级**|免密码登录，配置别名|
|ssh-keygen|生成SSH钥匙,包括公钥（id_isa.pub)和私钥(id_rsa)，免密码登录|
|ssh-copy-id -p port ghggfuser@remote|上传公钥到服务器(id_ras.pub)|
|非对称加密算法|公钥加密的数据用私钥解密；私钥加密的数据用公钥解密|
|配置别名|在~/.ssh文件夹下创建config文件，gidit config，输入配置信息|
|配置信息｜host mac（指定的别名)  
HostName ip地址  
user （远程计算机用户名）  
   port 22(端口)|

### 用户权限相关设置。
####   
|序号|权限|英文|缩写|数字代码|
|:--:|:--:|:--:|:--:|:--:|
|01|读|read|r|4|
|02|写|write|w|2|
|03|执行|excute|x|1|
  
|command|meaning|
|:--:|--------|
|ls -l|权限，硬链接数，拥有者，组，大小，时间，名称|
|硬链接数|可以有几种方式到达文件或目录|
|chmod|chmod +/-rwx 文件名/目录名|
|执行文件的方法|./01.py|
|目录没有可执行权限|不能访问|
|目录没有可读权限|ls时不能显示目录下的文件内容|
|目录没有可写权限|不能在目录下添加文件或目录|
|**超级用户**|root:专门系统维护和管理|
|sudo|substitute user do;标准用户使用另一个用户的身份|
|组操作|标准用户要+sodu|
|groupadd|添加组|
|groupdel|删除组|
|cat etc/group|查看组的信息|
|chgrp|change group|
|chgrp -R 组名 文件/目录名|递归修改文件/目录的所属组|
|||
|useradd -m -g 组 新建用户名|添加新用户；-m：自动建立用户家目录;-g:指定用户所在组|
|passwd 用户名|设置用户密码|
|userdel -r 用户名|删除用户|
|cat /etc/passwd ｜grep 用户名|确认用户信息,用户信息保存在/etc/passwd文件中|
|id 用户名|查看uid(用户代号）,gid（组代号） |
|/etc/passwd|密码信息存在此文件|
|/etc/group|组信息存在此文件|
|passwd文件信息|用6个冒号组成7个信息：1.用户名，2.密码（x表示加密的密码），3.UID（用户标识），4.GiD（组标识），5.用户全名或本地账户，6.家目录。7.登录使用的Shell。|
|who|当前所有登录的用户列表|
|whoami|当前登录用户的账户名|
|usermod|修改用户的主组/附加组和登录Shell|
|usermod -g 组 用户名|修改用户的主组（passwd中的GID）|
|usermod -G 组 用户名|修改用户的附加组|
|usermod -s /bin/bash|修改用户登录Shell|
|dash和bash|ubuntu默认是dash，切换为bash比较好|
|**which**|查看执行命令所在位置|
|/etc/passwd|是保存信息用的文件|
|/usr/bin/passwd|是可执行文件|
|bin和sbin|bin下保存可执行文件，sbin保存系统重要的可执行文件|
|usr/bin或use/sbin|是在系统安装后，后期安装的可执行文件|
|su|切换用户|
|su - 用户名|- 可以切换到用户家目录|
|su -|直接切换到root|
|||
|修改文件权限命令|chown,chgrp,chmod|
|chown|修改所有者chown 用户名 文件名｜目录名|
|chgrp|修改所属组chgrp -R 组名 文件名｜目录名|
|chmod|修改权限chmod -R 755 文件名｜目录名|
|r|4|
|w|2|
|x|1|
|777|u=rwx,g=rwx,o=rwx|
|755|u=rwx,g=r-x,o=r-x|
|644|u=rw-,g=r--,o=r--|
|||
  
### 系统信息相关命令：
#### 
|command|meaning|
|:--:|------|
|date|查看系统时间|
|cal|查看日历 -y|
|df -h|disk free|
|du -h [目录名]|disk usage|
|-h|以人性化的方式|
|进程|当前正在执行的程序|
|ps aux|process status 查看进程的详细状态|
|a|终端上的所有进程,包括其他用户进程|
|u|显示进程的详细状态|
|x|显示没有控制终端的进程|
|top|实时显示当前正运行的程序，q 结束|
|kill [-9] 进程代码|终止指定进程代号（PID)的进程，-9表示强制停止|
|find [路径] -name "*1*.py"|查找文件|
|**软连接**|类似于快捷方式|
|ln -s 被链接的源文件 链接文件|建立文件的软连接;**源文件一定要使用绝对路径**|
|**硬链接**|ln 被链接的源文件 链接文件：相当于文件的另一个名字|
|linux中，文件名和文件数据是分开存储的||
|||
|tar|**打包**文件名：.tar|
|tar:只负责打包，不负责压缩|tar -cvf 打包文件名.tar 被打包的文件/路径|
|tar -xvf 打包文件.tar|解包命令|
|tar -cvf py.tar 01.py 02.py 03.py|tar -xvf py.tar|
|gzip|**压缩**文件名.tar.gz|
|tar -zcvf 打包文件.tar.gz 被压缩的文件/路径|tar -zxvf 打包文件tar.gz|
|bzip2|-j .tar.bz2 -C(指定解压缩路径)用法和gzip一样|
|apt|Advanced Packaging Tool|
|sudo apt install 软件包|安装软件|
|sudo apt remove 软件名|卸载软件|
|sogu apt upgrade|更新已安装的包|
|配置软件源|国内镜像服务器，阿里、清华、搜狐|

### 域名是IP地址的别名
### 端口号：不指定端口，就使用默认端口。22；80；443；21：

## KALI linux学习：  
#### 制作U盘镜像：推荐unerbootin。
#### 从：[kali官网](https://www.kali.org)上下载   

## 使用ssh，Ubuntu系统先安装ssh才可以使用。   
  
	sudo apt-grt install openssh-server
	sudo etc/init.d/ssh start
	ps -elgrip ssh
   
	更改端口号要先stop，之后改端口，之后再start  









  
绝对路径：/开始的
相对路径：前面没有/  
同一个目录中，文件和目录不可以重名。  

