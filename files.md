#mkdir
『 mkdir -p /home/bird/testing』则系统会自动的帮你将 /home, /home/bird, /home/bird/testing 依序的建立起目录！并且，如果该目录本来就已经存在时，系统也不会显示错误讯息喔！挺快乐的吧！ ^_^ 

#PATH
PATH=”$PATH”:/root
临时加入path路径

#mv
```shell
mv bashrc bashrc.old 
mv bashrc bashrc2 /tmp
```

<==将 bashrc 与 bashrc2 移动到 /tmp 这个目录下！请注意，最后一个才是最终的目标，其他的都是 SOURCE

#basename
```shell
basename /usr/local/etc   ==>etc
```
这个指令颇有点意思～他可以将一个目录或档案的最后一个咚咚秀出来！所以，未来如果你有要使用变量，并且取出最后一个数据(不论是档案还是目录)

#dirname
```shell

[root @test /root ]# dirname [目录] 
参数说明： 
范例： 
[root @test /root]# dirname /usr/local/etc 
/usr/local 
```
这个指令恰恰与 basename 相反的啦！呵呵！很好玩吧！这部份也最常用在我们第三部分要讲的 Shell 的学习中喔！用最多的地方应该是 scripts 啦！

#观看内容
cat  由第一行开始显示档案内容 
tac  从最后一行开始显示，可以看出 tac 是 cat 的倒着写！ 
more 一页一页的显示档案内容 
less 与 more 类似，但是比 more 更好的是，他可以往前翻页！ 
head 只看头几行 
tail 只看尾巴几行 
nl   显示的时候，顺道输出 行号！ 
od   以二进制的方式读取档案内容！

#搜寻档案或目录
which   查看可执行文件案的位置 
whereis 查看档案的位置 
locate  配合数据库查看档案位置 
find    实际搜寻硬盘去查询文件名

```shell
panxiaomingdeMacBook-Pro:~ cp$ which psql
/usr/local/bin/psql
```