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
|grep 


  
绝对路径：/开始的
相对路径：前面没有/  
同一个目录中，文件和目录不可以重名。  

