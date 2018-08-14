# Principle of Microcomputer

[慕课网微机原理学习课程](https://www.icourse163.org/learn/JLU-1002056024?tid=1002784152#/learn/announce)

## 章一 微型计算机基础知识

### 微型计算机系统简介

(1)微型计算机的组成：微处理器、总线、输入输出、存储器

(2)微处理器功能：在设备间传输数据、进行简单的逻辑运算、控制程序流向

(3)常用的存储器有：动态随机存储器、静态随机存储器、高速缓冲存储器、只读存储器、闪速存储器

(4)存储容量与地址总线的数量相关。

(5)由于输入输出设备一般与主机的信号电平格式、时序、工作方式、传输速度不同，故在I/O与微处理器间一般还有I/O接口。

(6)微型计算机是总线型结构的计算机系统。

(7)系统总线用于在CUP、I/O、存储器间传输信息。根据传输信息的类别又分为数据总线、控制总线和地址总线。

(8)数据总线（DB）：进行数据传输。

(9)地址总线（AB）：向I/O和存储器传送地址信息，是单向总线。

(10)控制总线（CB）：用来传送时序信号、状态信号和控制信号。每一根控制信号线是单向的，但是总体看来，CB是双向的。

### 数制与运算

(1)进位计数制三个要素：基数、位权、数码。

(2)对于任何一个进位计数制都可以表示为一个展开多项式(按权展开多项式)。

(3)十进制数转换为非十进制数方法：整数部分（除X取余）、小数部分(乘X取整)。

(4)计算机中的二进制乘法运算是利用左移位+累加部分积实现的(加法运算和左移位运算)。

(5)计算机中的二进制除法运算是利用右移位+累减部分商实现的(减法运算和右移位运算)。

(6)一个n位的无符号二进制数的表示范围是:     0 <= X <= 2^n-1

   一个n为的有符号二进制数的表示范围是：    -(2^(n-1)-1) <= X <= 2^(n-1)-1
   
   >如果数值溢出，微型计算机中，会将微处理器中的CF标志位置1。
   
(7)带符号数的表示方法：原码、反码、补码。
   原码（表示范围为-127～127）：最高为符号为（1：负 0：正），数值部分为真值得绝对值。
   
   反码（表示范围为-127～127）：正数的反码与原码相同，负数的反码为原码符号位保持不变，其余各位按位取反。
   
   补码（表示范围为-128～127）：正数的补码与原码相同，负数的补码为它的反码加1。
   
   >补码特点：
   
   >         1> 原码和反码表示的0有+0和-0之分，即0的表示不唯一；而补码的0是唯一的，没有+-0之分。
   
   >         2> 一个负整数（或原码）与其补数（或补码）相加，和为模。
            
   >         3> 对一个整数的补码再求补码，等于该整数自身。
            
   >         4> 计算机系统中一律用补码来表示和存储。
   
   > 由补码求真值的方法：
   
   >         1>按权累加 
   
   >         2>求它的补码得到原码，按权求真值。
                     
   补码的位权：
   
   ![Loading...](https://github.com/BasenLi/Principle-of-Microcomputer/blob/master/src/Photo/%E4%BD%8D%E6%9D%83.png?raw=true)
                     
 (8)补码的运算规则：
 
   ![Loading...](https://github.com/BasenLi/Principle-of-Microcomputer/blob/master/src/Photo/%E8%A1%A5%E7%A0%81%E8%BF%90%E7%AE%97%E8%A7%84%E5%88%99.png?raw=true)
 
 (9)如何判断运算时带符号数的溢出：
 
   >运算时计算符号位的进位记为C7，计算数值位的最高位记为C6，再用C6⊕C7，如果计算结果为1，则表明运算会溢出。
   
   >在微型计算机中，如果存在运算溢出，会将微处理器中的OF标志位置1,。
                     
       
                     
                     
   

   
   

   
   


