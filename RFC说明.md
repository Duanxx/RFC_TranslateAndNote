# RFC说明

标签（空格分隔）： RFC

@author : duanxxnj@163.com
@update time : 2017-02-14

---

Request For Comments (RFC），是一系列以编号排定的文件，几乎所有的因特网标准都收录在RFC文件之中，如果你想成为网络方面的专家，那么RFC无疑是最重要也是最经常需要用到的资料之一，所以RFC享有网络知识圣经之美誉。一言以蔽之，想要学网络协议，就看RFC。

其官网为:[https://www.rfc-editor.org/][1]

国内china-pub翻译了[RFC1~RFC3093][2]，国内还有一个[RFC协议分析网站][3]，不过这两个网站貌似都已经在几年前就停止更新了。

---

---

下图是RFC官网中，RFC文档搜索栏，从这里可以看出，RFC文档一共有6个类别，而这些类别其实是当前文档所处的状态。
![image_1b8t30us8d81d371t93noo1thf9.png-37.5kB][4]

 - Standard Track , 简称STD RFC，按照[RFC1311][5]的定义，STD RFC是指那些已经或者致力于成为Internet标准的RFC。经过完全Internet标准化过程的RFC就可以有STD编号，且STD编号是不变的，但其涉及到的 RFC文档可能不只一个。
 
 - Best Cueernt Peactice, 简称BCP RFC，其定义在[RFC1818][6]中，主要是在STD RFC之外规定的，各种不同组织、不同使用目和使用规则的协议。
 
 - Informational, 是与Internet标准有关的一般性信息的说明文档，如前面的[RFC1311][7]和[RFC1818][8]都是这类文档。
 
 - Experimental，一般是反映一些研究和开发的成果。
 
 - Historic，是一些被新的标准取代或者是已经过时废弃不用的标准。
 
 - Unknown，是一些被提出但是未被采用或关注，然后就没有然后的标准，也不知道怎么分类比较好，就直接Unknown了。

---

---

从下图中可以看出，STD RFC还可以细化为三个级别：
![image_1b8t5cog91qoim0gtsc1fj11enum.png-24.4kB][9]

 1. Proposed Standard，基本成熟，但还需要进一步的试验证实其可行性。除非是用来验证该协议的可行性，不要将其视为标准实现
 2. Draft Standard，需要两个独立的，而且具有相互操作性的实例验证该协议的每一个方面。可以将其视为最终的标准草案
 3. Internet Standard，最终的Internet标准，同时赋予一个STD编号


---

---

最后需要说明一点，从下图中可以看出，任何一个RFC文档，都有可能已经是一个过时的文档，或者被其他文档所更新，或者被其他文档所取代，查阅RFC文档的时候需要注意后面的文档说明。
![image_1b8t5nvsq12hq1c6dskbqiu11v71g.png-91kB][10]


  [1]: https://www.rfc-editor.org/
  [2]: http://man.chinaunix.net/develop/rfc/default.htm
  [3]: http://www.cnpaf.net/index.html
  [4]: http://static.zybuluo.com/Duanxx/vy031xoiq1w2mftz1fjd2sb6/image_1b8t30us8d81d371t93noo1thf9.png
  [5]: https://www.rfc-editor.org/pdfrfc/rfc1311.txt.pdf
  [6]: https://www.rfc-editor.org/pdfrfc/rfc1818.txt.pdf
  [7]: https://www.rfc-editor.org/pdfrfc/rfc1311.txt.pdf
  [8]: https://www.rfc-editor.org/pdfrfc/rfc1818.txt.pdf
  [9]: http://static.zybuluo.com/Duanxx/xuybkab8oarfzg0nbq5iepw6/image_1b8t5cog91qoim0gtsc1fj11enum.png
  [10]: http://static.zybuluo.com/Duanxx/iua5x18c2gsq4i6rd2hzuqxd/image_1b8t5nvsq12hq1c6dskbqiu11v71g.png