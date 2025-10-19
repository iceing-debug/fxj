这个题目的call和jnz，jz跳转很多，我一个个手动nop了，然后还是无法F5反编译,就是因为还有这些黄色区域，

IDA无法判断这是数据还是代码，按U取消定义，然后按C转换成代码，P是重新定义函数。我在这里是按C转换成代码后就可以正常反编译了

![1760270900873](https://raw.githubusercontent.com/iceing-debug/fxj/master/1760270900873.png)



xor eax,eax    该指令会把eax寄存器清零

然后jz是eax为0的时候会跳转，那就相当于强制跳转jmp，所以中间跳过的代码就是没用的代码，起到了花指令的作用

xor eax,eax

jz   short loc_12000152F             为花指令形式

![](https://raw.githubusercontent.com/iceing-debug/fxj/master/1760270900873.png)

