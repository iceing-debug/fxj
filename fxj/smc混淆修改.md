for循环的地方是smc混淆处理的地方，可以使用idc处理，就从初始地址开始把smc处理过的段落处理回来就行

![1760241082510](https://raw.githubusercontent.com/iceing-debug/fxj/master/fxj/1760241082510.png)

比如下面这个图，就从0x11E9的地址开始，然后看smc处理了多少个地址

![1760241519461](https://raw.githubusercontent.com/iceing-debug/fxj/master/fxj/1760241519461.png)