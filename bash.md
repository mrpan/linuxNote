
env

显示目前系统中主要的默认变量内容 


history, !command

显示历史指令记录内容, 下达历史纪录中的指令 

source：

前面提过了，如果我需要将目前的配置文件的内容读入一次，需要重新 logout 再 login 才能够读入，那么有没有办法不注销而直接读入变量配置文件呢？当然可以，就使用 source 即可！
#ls -l />test1
就是将你目前的所得资料转到其他地方去就是了！例如我们常用的，将目前的屏幕输出数据转到档案中去，就可以这么写：『ls -l / > test 』，那个大于的符号『 > 』就是将输出结果导向到 test 这个档案中的意思啰！这个时候：


[test @test test]# ls -al >  list.txt  
将显示的结果输出到 list.txt 档案中，若该档案以存在则予以取代！ 
[test @test test]# ls -al >> list.txt  
将显示的结果累加到 list.txt 档案中，该档案为累加的，旧数据保留！

[test @test test]# ls -al 1> list.txt 2> list.err  
将显示的数据，正确的输出到 list.txt 错误的数据输出到 list.err 

[test @test test]# ls -al 1> list.txt 2>&1  
将显示的数据，不论正确或错误均输出到 list.txt 当中！ 

[test @test test]# ls -al 1> list.txt 2> /dev/null 
将显示的数据，正确的输出到 list.txt 错误的数据则予以丢弃！ 
注意！错误与正确档案输出到同一个档案中，则必须以上面的方法来写！ 
不能写成其他格式！

<  ：由 < 的右边读入参数档案；
>  ：将原本由屏幕输出的正确数据输出到 > 右边的 file ( 文件名 ) 或 device ( 装置，如 printer )去；
>> ：将原本由屏幕输出的正确数据输出到 >> 右边，与 > 不同的是，该档案将不会被覆盖，而新的数据将以『增加的方式』增加到该档案的最后面；
2> ：将原本应该由屏幕输出的错误数据输出到 2> 的右边去。
/dev/null ：可以说成是黑洞装置！ 