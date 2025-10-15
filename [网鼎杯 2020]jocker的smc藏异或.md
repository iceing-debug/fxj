![1760097503172](C:\Users\23671\AppData\Roaming\Typora\typora-user-images\1760097503172.png)

首先两个函数出错无法F5,打断点在第一个出错的函数上，然后IDA动态调试，

动态调式到下断点的函数处，如果函数是主要逻辑中的一部分就F7进入查看函数，如果是红色jump报错就F8步过

进入函数后函数头按U，把函数代码全选按c，然后函数头P重新定义函数，修复成功。第二个有个红色的jump出错，把jump的那个代码patch成90（nope填充），按P修复成功



flag有两段，这段是后面一段的代码，已知五个字符串中最后一个为}

```
# XOR加密的特点：
# 如果 A ^ key = B
# 那么 A = B ^ key
# 而且 key = A ^ B
```

​    

```python
 
hh = 'hahahaha_do_you_find_me?'
v2 = [0x0E, 0x0D, 0x9, 0x6, 0x13, 0x5, 0x58, 0x56, 0x3E, 0x6,
      0x0C, 0x3C, 0x1F, 0x57, 0x14, 0x6B, 0x57, 0x59, 0x0D]
flag = []
 
 
for i in range(19):
    flag.append(chr(v2[i] ^ ord(hh[i])))
```