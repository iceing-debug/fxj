“call $ + 5” 和 “retn” 这两条指令的花指令处理

call $ + 5上方会有push，也要一起nope。retn下方会有pop，可能还有有一些数据，也要一起nope掉

首先先nope，然后找到函数头按U转换成数据，然后从函数头开始到nope过的所有部分全选，然后按C转换成代码，点金force，然后最后再找到函数头按P重新定义，一般就可以反汇编成功

![1760173460314](https://raw.githubusercontent.com/iceing-debug/fxj/master/fxj/1760173460314.png)