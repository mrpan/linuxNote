# linuxNote
常用linux命令

查看文件夹大小
```shell
 du -h --max-depth=1
```

显示日期的指令： date
显示日历的指令： cal
简单好用的计算器： bc

#chgrp ：改变档案所属群组 
```shell
chgrp users file
```
chown ：改变档案所属人 ,也可以改变群组
```shell
chown –R root:root tmp
```
chmod ：改变档案的属性、 SUID 、等等的特性

-rwxrwxrwx
r:4 
w:2 
x:1 
```shell
chmod 777 file
```

符号类型改变档案型态 
还有一个改变属性的方法呦！从之前的介绍中我们可以发现，基本上就九个属性分别是(1)user (2)group (3)others 三群啦！那么我们就可以藉由 u, g, o 来代表三群的属性！此外， a 则代表 all 亦即全部的三群！那么读写的属性就可以写成了 r, w, x 啰！也就是可以使用底下的方式来看：

可以使用『 chmod u=rwx,g=rx,o=r filename 』来设定
