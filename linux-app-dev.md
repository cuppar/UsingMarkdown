> version: Redhat linux 9.0 (recommonded) 
> http://distrowatch.com
> - ftp:zhuyp_std  
> - Linux程序设计 中文第4版 Neil Matthew, Richard Stones 2010 JUN
> - Linux应用开发技术详解 2006 FEB
> - Linux操作系统应用与开发教程 清华大学出版社 2016 MAY  



## Week 1
---
### Linux Introduction
Author: Linux Torvalds  
Time: 1991 SEPT

features:
- open-source
- multi-task
- multi-user
- network  

### Linux Program
- executable file: judged by property
- script

### Linux Basic Command
#### help command
- 查看命令帮助：`命令名 --help`  
- 查看命令帮助：`man 命令名`
- 在线帮助：`info 命令名`
- 显示用户id：`whoami`
- 显示主机名称：`hostname`
- 显示操作系统名称：`unanme`

#### 文件系统命令
mount / umount 命令
- 挂载：`mount [参数] 设备名 挂载目录`
- 卸载：`umount 卸载目录`

ls 命令  
- 显示所有文件以及详细信息：`ls -al`

rmdir / mv / rm 命令
- 删除**空**目录：`rmdir 目录名`  
- 重命名或移动位置：`mv [参数] file1 file2`
- 删除文件：`rm [参数] file-list`

chmod 命令
- 更改文件或目录的访问权限，使用者是root或文件的所有者
- -R 递归处理文件夹所有内容
- 符号模式：`chmod <who><operator><privilege> file`
- 数字模式：`chmod 777 file`

chown 命令
- 更改一个或多个文件或目录的owner和group，使用者是超级用户
- 把文件shiyan.c的所有者改为tim：`chown tim shiyan.c`

ps 命令
- 显示当前进程的动态，使用权限是所有使用者
- 格式：`ps [options]`
- 显示所有包含其他使用者的进程：`ps -aux`
- 显示进程详细信息：`ps -l`

who 命令
- 显示系统中有哪些登陆用户

kill 命令
- 进程终止命令
- 格式：`kill [options]`

& 进程和作业控制命令
- 可以控制进程在后台执行，命令与&之间不需要空格
- 执行后会把PID和状态返回给前台

echo 命令
- 用来在屏幕上显示字符串

### Shell的环境变量
- 存在`/etc/profile`和`/etc/csh.cshrc`
- 可以通过`export`设置临时变量

### 输入输出重定向
- 输入重定向 <
  - 用来断开键盘和标准命令输入之间的关联
- 输出重定向 >
  - 用来断开屏幕和标准命令输出之间的关联
  - 用 >> 来追加输出至目标文件末尾

### 管道命令
- 可以用管道操作符“ | ”来链接进程
- command1 | command2 | command3 ...

### 特殊符号的使用
- 分号 `;` 用来在一个命令行上运行多个命令，顺序执行
- 反斜线 `\` 用来分行输入长命令
- 波浪线 `~` 用来代指用户主目录
- `&` 用来后台执行命令
- `&&` 和 `||`表示使用与和或的策略执行命令

> 任务：  
> 编写shell脚本，查询某个文件的权限，网络状况，端口情况，并同时把这些信息写入到文件a.dat中

### shell程序的内置参数
- `$0`: 程序名字
- `$#`: 参数数目
- `$?`: 退出状态码
- `$*`: 参数列表