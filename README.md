# linux-
note for linux basic instructions

## 基础指令 
 
# 1.ls 指令
用法：
1.#ls       作用：列出当前目录下的所有文件名和文件夹名。
    
2.#ls 路径   作用：列出目标路径下的所有文件名和文件夹名。
（路径可以是绝对路径也可以是相对路径）
（相对路径中 ./表示当前路径 ，../表示上一级路径）

3.#ls 选项 路径   作用：以选项的格式列出指定路径下文件和文件夹的名字。
 常见的有 #ls -l 路径  #ls -la 路径   -l 表示list ,以详细的列表形式列出， -a 表示显示所有文件和文件夹（包括隐藏的）。
 列表中开头字符为d 的是文件夹，为-的是文件。  .开头文件时隐藏文件。
 
4.#ls -lh 路径    作用：列出指定路径下的所有文件名和文件夹名，其中文件大小以最合适的单位显示。

ls 列出的文件颜色 ：  蓝色表示文件夹，黑色表示文件，绿色表示拥有所有权限 。

# 2.pwd 指令  （print  working directory) 

   用法： #pwd  打印当前工作目录 （绝对路径）
   
# 3. cd 指令  （change directory)
   用法: #cd  路径  
   作用：切换到指定路径。
   cd ~ 切换到家目录。
 
 
# 4.mkdir 指令（make directory ）
   用法 
   1.#mkdir  路径
   作用 在指定路径下创建文件。
   
   2.#mkdir -p 路径
   作用 实现一次性创建多层不存在的文件夹。
   
   3.#mkdir 路径1 路径2 路径3
   作用  一次性创建多个。
 
# 5. touch 指令 （创建文件） 
   用法
   #touch 文件路径 （可创建多个）
   作用：创建文件在指定目录下
   
# 6.cp 指令  （复制并粘贴）
   用法
   #cp  被复制的路径  粘贴的路径 （复制文件夹要加上 -r)
   作用：复制文件到目标路径
   
# 7.mv 指令 （move）
  用法 类似cp指令
  #mv 需要移动的文件的路径   移动到的路径  （如果路径不变可以改变文件的名字）
  
# 8. rm 指令 （remove）
   用法
   #rm  选项  需要移除的文件路径
   1. #re -f  (强制删除，无需确认）
   2. #re -r  (删除目录）  
   rf  可以一起用 
   * 通配符 
  
# 9. vim 指令
   用法
   #vim 文件路径 
   作用 用vim打开一个文件
   退出vim 文件： 在没有按下其他按钮时 按下shift + ：再输入q键退出。
   
# 10. 输出重定向 
 一般的指令的结果输出在终端上，使用输出重定向可以把结果保存在文件里。
 “>”覆盖输出
 “>>”追加输出
 如果目标文件不存在，也会创建文件并输出结果。
  
# 11. cat 指令
   用法
   1.#cat  文件路径
     作用：输出文件内容到终端
   2.#cat   文件路径1  文件路径2 ... 文件路径n  > 文件路径  (输出重定向）
     作用：输出多个文件内容到一个文件中。
   
 
## 进阶指令
 
# 1. df 指令
 用法  
 1. #df  
 作用： 查看硬盘空间
 2. #df -h
 作用： 查看以合适的单位显示硬盘空间使用情况
 
 
# 2.free 指令
用法
1. #free 
 作用 ： 查看内存使用情况  (swap 为临时内存，内存不够用时用磁盘空间来代替）
 
2. #free -选项  
 作用 ：以选项单位显示内存使用情况   （ m --mb  , g -- gb )
   
# 3.head 指令
用法 
1. #head  文件名
 作用：查看文件的前十行
2. #head -n 文件名
 作用 ：查看文件的前n行
 
# 4.tail 指令
用法
1. #tail  文件名
  作用：查看文件的尾10行
  
2. #tail  -n 文件名
  作用：查看文件的尾n行
  
3. #tail  -f 文件路径
  作用 ：   动态查看文件的变化
# 5. less 指令
用法
#less 文件路径
作用 ： 查看文件，输出较少的内容，按下辅助键查看更多。

# 6. wc 指令
用法
#wc  -l,-w,-c 
作用： -l 表示行数， -w 表示单词数 ， -c 表示字节数 。
# 7.date 指令
用法
1.#date   
作用： 输出时间（年月日小时分。。）

2.#date +%F (F要大写） 或者 #date "+%Y-%m-%d" (冒号可以去掉）
作用： 输出年月日。

3.#date "+%F %T" 或者 #date "+%Y-%m-%d %H:%M:%S"
作用： 输出年月日小时分秒。

4.#date -d "+1 day" "+%Y-%m-%d %H:%M:%S" 
作用：输出一天后的时间。

# 8.cal 指令
用法
1. #cal 
 作用： 直接输出当前月份的日历。
 
2. #cal -3 
 作用：输出上一个月，本月和下一个月的日历。
 
3. #cal -y 年份    
 作用：输出指定年份的日历。
 
4. #cal -m 
  作用：输出时每个星期开始是星期一。
  
# 9. ctrl + l /clear  指令
用法
#clear 或者 CTRL + l 
作用： 清屏。

# 10.管道
管道符 “|”
作用：把|前的命令的输出当作|后命令的输入。
用法：
1. ls |less
作用：ls 输出当前目录的文件名，less 分页输出 ————分页输出当前目录文件名。

## 高级指令

# 1.hostname 指令
用法
1.#hostname 
作用：输出完整的主机名。
2.#hostname -f
作用：输出当前主机名中的全限定域名。

# 2.id指令 查看一个用户的基本信息（包括用户iD,用户组 id ,附加组id )
用法
1. #id ( 默认查看当前执行该命令的用户的基本信息）
2. #id 用户名    显示指定用户的基本信息。

# 3.whoami 指令
显示当前登录的用户名，用于获取当前的操作的用户名。

# 4.ps -ef 指令 
用法
作用：主要是查看服务器的进程信息。 
#ps -e -f 
-e ：等价于“-A”，表示列出全部的进程。
-f : 显示全部的列（显示全字段）
列的含义：
UID：该进程执行的用户id
PID: 该进程的父级进程id，如果一个程序的父级进程找不到，该程序的进程称之为僵尸进程；
C： CPU的占用率，其形式是百分数；
STIME:进行的启动时间；
TTY：终端设备，发起该进程的设备识别符号，如果显示“？”则该进程不是由终端设备发起的；
TIME:进程的执行时间；
CMD: 该进程的名称或者对应的路径；

# 5.top 指令
作用：  查看服务器的进程占的资源。
用法：
1.#top  （动态显示）
表头含义：
PID:进程id；
USER:该进程对应的用户；
PR:优先级；
VIRT:虚拟内存；
RES:常驻内存；
SHR：共享内存；
S：表示进行的状态（sleeping）
%CPU:表示内存的占用百分比；
%MEM:表示内存的占用百分比；
TIME+:执行的时间；
COMMAND:进程的名字或路径；


           
