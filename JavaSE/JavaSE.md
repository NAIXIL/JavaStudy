---
number headings: auto, first-level 1, max 6, 1.1
文件名: Java基础知识
作者: 李显
邮箱: lixian_shandong@126.com
创建时间: 2022-04-29 15:33
---


# 1 基本数据类型
## 1.1 基本数据类型
1. 整数类型：
    1. byte: 8bit, -128~127
    2. short: 16bit, -32768~+32767, $-2^{15}\sim2^{15}-1$
    3. int: 32bit,  $-2^{31}\sim2^{31}-1$
    4. long: 64bit, $-2^{63}\sim2^{63}-1$
2. 字符和字符串类型：
    1. char, 16bit, $0\sim2^{16}-1$
    2. String, 是类，所创建的字符串本质是对象
3. 小数类型
    1. float: 32bit, 
    2. double: 64bit, 
4. 布尔类型：boolean b = true;

## 1.2 类型转换

1. 隐式类型转换：
    - byte $\rightarrow$ short(char) $\rightarrow$ int $\rightarrow$ long $\rightarrow$ float $\rightarrow$ double
2. 显式类型转换：
   ```java
   int b = 128;
   byte a = (byte) b;
   ```


# 2 运算符
## 2.1 赋值和算术运算符
```java
// 赋值：=
// 算术运算符+, -, *, /, % 
```
### 2.1.1 +号用于拼接字符串
字符串放在+号前面，后续的内容被当作字符串处理。

```java
byte a3 = 10;
byte b3 = 126;
System.out.println("lixian" + b3 + a3);
System.out.println(b3 + a3 + "lixian" );
System.out.println("lixian" + (b3 + a3));
```
运行结果：
```shell
lixian12610
136lixian
lixian136
```

## 2.2 关系运算符
```java
// 大于、小于、等于：> < ==
// 大于等于、小于等于、不等于：>= <= !=
// 比较的结果是布尔类型：true, false
```

## 2.3 逻辑运算符
- 逻辑运算符：
    1. 与（&&）：两边同时为真则为真，否则为假；
    2. 或（||）：两边至少有一个为真则为真，否则为假； 
    3. 非（!）：反转右侧表达式的真假值。
## 2.4 位运算符
- 位运算
    1. 按位与，&：二进制的对应位做与运算。
    2. 按位或，|：二进制的对应位做或运算。
    3. 按位异或，^：二进制的对应位做异或运算。（异或：相同为0，不同为1。）
    4. 按位非，~：二进制的每位做非运算。

```java
byte a8 = 10; // 二进制表示：1010  
byte b8 = 15; // 二进制表示：1110  
System.out.println(Integer.toBinaryString(a8 & b8));  
System.out.println(Integer.toBinaryString(a8 | b8));  
System.out.println(Integer.toBinaryString(a8 ^ b8));  
System.out.println(Integer.toBinaryString(~a8));
```
输出：
```shell
1010
1111
101
11111111111111111111111111110101
```
## 2.5 三目运算符
形式：表达式（返回的值需布尔类型）? 为真的返回值 : 为假的返回值

```java
int a9 = 7;  
int b9 =15;  
String str9 = a9 < b9 ? "Yes" : "No";  
System.out.println(str9); // Yes
```



# 3 流程控制
## 3.1 选择结构if、switch
1. if... else...
```java
if (判断){
    // 执行
}else if (判断){
    // 执行
}else{
    // 执行
}

```
2. switch 
    1. 注意case只能是固定的值，不可以是表达式。
    2. switch效率比if else更高。
    3. 如果没有运行代码、break，则可多个值进行聚合判定。
```java
switch(判断){
    case 值1:
        // 运行1
        break; // 用于跳出switch语句，不添加会导致程序继续向下运行
    case 值2:
        // 运行2
        break;
    defalut:
        // 运行
}
```
## 3.2 循环结构for、while
1. for
```java
for(int i =0; i<=5; i++){  
    System.out.println("lixian! " + i);  
}  
for (int i =9; i>4; i--){  
    System.out.println("xianli! "+ i);  
}
```
2. while
```java
/*  
* while 先判断，后执行  
* do while 先执行，后判断  
* */  
int a0 = 5;  
while (a0 > 1){  
    System.out.println(a0);  
    a0--;  
}  
  
int a1 = 5;  
do {  
    System.out.println(a1);  
    a1--;  
}while (a1 > 1);
```

**break关键字会跳出循环，执行后续语句；continue会跳过本次循环的后续语句，继续执行下一次循环。**








