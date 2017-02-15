# RFC20 用于网络交换的ASCII格式

标签（空格分隔）： RFC

@author ： duanxxnj@163.com
@time : 2017-02-15

---

---

ASCII format for Network Interchange
用于网络交换的ASCII格式

[TOC]

一句话，我们建议使用标准的7位ASCII编码，并通过高位补0的方式，将7位ASCII编码扩展成为8bit，以得到一个完整的字节。这样在主机之间做基本连接的时候，就可以直接使用USAS X3, 4-1968中已定义好的标准编码。一行字符的结束字符是由远程主机定义的，例如，SRI使用"."(ASCII X'2E' 或者 2/14)来作为行的结束字符，而UCLA则使用 "回车"(X'OD' 或者 0/13)作为行的结束字符。

>注：SRI是一个研究机构；UCLA是加利福尼亚大学洛杉矶分校。可以看出，当初网络刚开始兴起的时候，基本的字符编码还并没有统一，所以才会有这篇文章，用于统一字符编码，以及一行字符的结束符。这篇文章是UCLA于1969年提出的，所以后后来使用的就是“回车”了

-
>注： 关于“回车”（carriage return）和“换行”（linefeed）这两个概念很有意思。在计算机还没有出现之前，有一种叫做电传打字机的玩意，每秒钟可以打10个字符。但是它有一个问题，就是打完一行换行的时候，要用去0.2秒，正好可以打两个字符。要是在这0.2秒里面，又有新的字符传过来，那么这个字符将丢失。于是，研制人员想了个办法解决这个问题，就是在每行后面加两个表示结束的字符。一个叫做“回车”，告诉打字机把打印头定位在左边界；另一个叫做“换行”，告诉打字机把纸向下移一行，这就是“换行”和“回车”的来历。
      后来，计算机发明了，这两个概念也就被般到了计算机上。那时，存储器很贵，一些科学家认为在每行结尾加两个字符太浪费了，加一个就可以。于是，就出现了分歧。Unix系统里，每行结尾只有“换行”，即“<\n>”；Windows系统里面，每行结尾是“ <回车><换行>”，即“\r\n”；Mac系统里，每行结尾是“<回车>”,一直沿用至今

---

---

USA Standard Code for Information Interchange
美国信息技术标准编码（ASCII）

## 1 使用范围
本字符编码集用在各信息处理系统、通讯系统及相关设备之间的一般信息交换上。

## 2 标准编码

![image_1b8vm218ugrv1glt1d1k8ipiei9.png-110.9kB][1]

>注：由于ASCII编码的最高位并没有被使用，所以也有一些基于ASCII扩展的编码方式，比如扩展了[“僧伽罗语”的编码][2]，就是使用了最高位做了编码扩展。

##3 字符表示和编码定义
标准的7位字符编码定义：$b7$是最高位,$b1$是最低位，举个例子：
字符$K$在ASCII码表示是第11行，第4列，其二进制表示为

-----------------![image_1b8vniokg172f6uc1p58vi21kdhm.png-8.7kB][3]

字符在ASCII码表中的位置，也可以作为字符的表示方式，还是字符$K$，由于其在第11行，第4列，所以可以表示为“column 4, row 11”或者是“4/11”

编码表中的$(b4、b3、b2、b1)$所对应的十进制数，就是编码表的行号;而$(b7、b6、b5)$所对应的十进制数，就是编码表的列号。

上面的编码表可以简写为：ASCII或者USASCII

ASCII（发音为as’-key）、USACII（发音为yous s as’-key）的具体意义，通常是由其最新的编码标准确定，为了明确的指明一个编码标准，一般会在其后添加两个数字，以代表该编码方式发布的年份，比如：“ASCII 63”或“USASCII 63”。

>注：现在所使用的ASCII编码最终确立于1967年，然后再没有改变过，也就是“ASCII 67”

## 4 图例

>注：图例的英文原文是“Legend”，这里将其翻译为图例并不好，但是我没有想到更好的翻译，暂且先用这个

###4.1 控制符

|  代码        | 英文解释 | 中文解释|
|:-------------:|:-------------:| :-------------:|
| NULL     | null |空字符 | 
| SOH      |   Start of Heading (CC)    | 标题开始（通讯控制） |
| STX | Start of Text (CC)    |   文本开始（通讯控制）|
| ETX  | End of Text (CC)    |   文本结束（通讯控制）|
| EOT  | End of Transmission (CC)    |   传输结束（通讯控制）|
| ENQ  | Enquiry (CC)    |   查询（通讯控制）|
| ACK | Acknowledge (CC)   |   应答（通讯控制）|













  [1]: http://static.zybuluo.com/Duanxx/sfp93c1fb9j58l6yposayoy6/image_1b8vm218ugrv1glt1d1k8ipiei9.png
  [2]: https://www.researchgate.net/publication/279057491_UNICODE_Standard_Code_for_Information_Interchange
  [3]: http://static.zybuluo.com/Duanxx/7kgqn2jmfugwxwfc92b6eh03/image_1b8vniokg172f6uc1p58vi21kdhm.png
