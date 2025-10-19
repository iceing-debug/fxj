

![img](https://raw.githubusercontent.com/iceing-debug/fxj/master/fxj/7770dc60a3386cb240c48314bd0f190a.png)

注意地址和用于干扰的函数的旁边有没有合适的函数

```cpp
#include<iostream>
#include<cstring>
#include<stdio.h>
#include<unistd.h>
#include<fstream>
using namespace std;
 
int main(){
    string a = "Iodl>Qnb(ocy\x7Fy.i\x7F";
    a += "d`3w}wek9{iy=~yL@EC";
    for(short int i = 0; i < a.length(); i ++){
        cout << char(int(a[i]) ^ i);
    }
    char flag[] = {0x40,0x35,0x20,0x56,0x5D,0X18,0X22,0X45,0X17,0X2F,0X24,0X6E,0X62,0X3C,0X27,0X54,0X48,0X6C,0X24,0X6E,0X72,0X3C,0X32,0X45,0x5B};
    char key[4];
    key[0] = 'f' ^ flag[0];
    key[1] = 'l' ^ flag[1];
    key[2] = 'a' ^ flag[2];
    key[3] = 'g' ^ flag[3];
    cout << endl;
    for (short j = 0; j <= 24; ++j )
        cout << char(flag[j] ^ key[j % 4]);
}
```



![1759994102921](https://raw.githubusercontent.com/iceing-debug/fxj/master/fxj/1759994102921.png)



两个byte字节数据连在一起了，地址是连着的，然后两个一共是25字节，也符合密文的要求