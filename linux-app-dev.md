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
`命令名 --help`  
`man 命令名`  
`info 命令名`: online help  
`whoami`: show user's id  
`hostname`: ...  
`unanme`: show name of os

#### file system command
`mount [参数] 设备名 挂载目录`  
`umount 卸载目录`  
`ls -al`: 显示所有文件以及详细信息  
`rmdir 目录名`: 删除**空**目录  
`mv [参数] file1 file2`: 重命名或移动位置
`rm [参数] file-list`: 删除文件  

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
