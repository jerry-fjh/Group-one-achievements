## 单字符实现

命令：ll，查看read文件

![1](1.png)

实现代码，关键代码

while(read(flag ,&buff ,1)!=0)//判断目标文件是否为空
write(out flag,&buff,1);//将目标文件按单个字符写入新文件
close(flag);close(out flag);//关闭目标文件和新文件

 ![2](2.png)

生成大文件命令big file

cat /etc/passwd /etc/group >> big_file

ls / >>big file

![3](3.png)

编译reaf_wzr .c并执行，生成test_file

![4](4.png)

## 数组实现

关键命令

while(read(flag ,buff ,sizeof(buff ))!=0)
write(out flag,buff,sizeof(buff));
close(flag);close(out flag);

![a](a.png)

执行read_wzr2文件，比较两种方法执行时间（已将练习时生成的文件删除）

![b](b.png)

由此可知按数组实现比单字符更快，效率更高。