---
number headings: auto, first-level 1, max 6, 1.1
文件名: Java基础知识
作者: 李显
邮箱: lixian_shandong@126.com
创建时间: 2022-04-29 15:33
---


# 1 基本数据类型
## 1.1 范围
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

1. **类型转换：**
    1. 隐式类型转换：
        1. byte $\rightarrow$ short(char) $\rightarrow$ int $\rightarrow$ long $\rightarrow$ float $\rightarrow$ double