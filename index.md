## Welcome to GitHub Pages

# 嵌入式工作室-Linux方向-第一期

#### [2020090905020吴维熙题目提交]



## 一、认识Linux

#### **1.了解操作系统的演化历史，区分并联系UNIX，GNU，Linux**

​	（参考资料查找：google，知乎，CSDN，主要靠CSDN）

​	比较全的一个：[](https://blog.csdn.net/weixin_33893473/article/details/91554024?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522160256062919725255557848%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=160256062919725255557848&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-2-91554024.pc_first_rank_v2_rank_v28&utm_term=%E4%B8%83%E7%A7%8D%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F%E7%9A%84%E5%8F%91%E5%B1%95%E5%8F%B2%E5%8F%8A%E7%89%B9%E7%82%B9&spm=1018.2118.3001.4187)

​	还有一个关于unix的，很清晰：[](https://blog.csdn.net/u010727746/article/details/56683181?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522160256074619724848329463%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=160256074619724848329463&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~first_rank_v2~rank_v28-1-56683181.pc_first_rank_v2_rank_v28&utm_term=unix%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F%E7%9A%84%E5%8E%86%E5%8F%B2%E6%BC%94%E5%8F%98&spm=1018.2118.3001.4187)

 	可以完整回答第一个问题。

#### **2.尝试叙述为什么我们要使用Linux，它有什么特性和优点**

##### ***一、Linux 的特性***

​	1、Linux系统的稳定性

  	  **Linux采取了许多安全技术措施**，其中有对读、写进行权限控制、审计跟踪、核心授权等技术，	这些都为安全提供了保障。Linux由于需要应用到网络服务器，这对稳定性也有比较高的要求，实际	上Linux在这方面也十分出色。

​	2、Linux系统的安全性

 	   Linux系统在设计的时候就是针对多用户环境的，所以对系统文件，用户文件都做了明确的区分，	每个文件都有不同的用户属性，**作为一个普通用户，通常只能读写自己的文件，而对一般的系统文	件只能读取不能改动**，一些敏感的系统文件甚至连读取都是被禁止的，这种设计从根本上保证了系	统的安全性，即使一个用户文件出现了问题，也不会殃及整个系统。

​	3、Linux软件安装的便利性 

  	 我觉得不用赘述

​	4、Linux软件资源消耗

   	由于**内核小**，因此他**可以支持多种电子产品**，如：Android手机，PDA等，资源消耗很少。

##### ***二、Linux系统的优势***

​	1、Linux系统所有组件的源代码都是自由的

  	（开源棒啊！再创作，再再创作，再再再创作） Android是一种基于Linux自由及开放源代码的操	作系统,主要用于移动设备。Android操作系统的发展带动了智能硬件的提高和更新。Android系统	采用分层架构,应用程序开发与Android系统开发耦合性不高,增强了应用程序开发的灵活性。

​	2、Linux系统能有效保护学习成果

​	   Linux**主力开发语言一直是C语言**，编辑器仍然是历史悠久的vi。虽然现在你可以使用任何一种语言	来为Linux系统贡献代码，但是它们的作用都是辅助性的，C语言作为这个系统的核心语言的地位没	有发生变化。而Windows平台则远远没有这么乐观。编程语言从古老的Basic到后来的VB,C++到现	在的C#，几年就更换一次，开发工具更是让人眼花缭乱，让人无从选择。无论你选择了哪种语言，	哪种开发工具两三年后你都不得不去学习新的工具的使用，新平台的特点，以跟上微软变化莫测的	脚步。

​	3、Linux系统的就业前景

  	  相比Windows平台开发，Linux平台在国内这方面的开发人员还很少，而Linux应用已经在我国全	面升温，所以前景还是蛮不错的。



## 二、接触Linux

> `背景：白得不能再白的小白 对电脑一窍不通的某女生……`
>
> `配置：win7 32位  已经废掉了的母上大人的旧电脑`
>
> `方式：虚拟机（以后要用新买的树莓派跑啦，芜湖）``（如果我配拥有新电脑的话，我打算用mac 23333）`
>
> `一些说（bao)明(yuan)：`
>
> `一些步骤因为摸索的太过投入，截图什么的是后来重现的，但是学习过程反映的完整度可能没法太保证......我尽力了`
>
> `作为从没接触过电脑，也不从打网游的白中白，下面每一步说来轻巧，但可能随随便便就花掉我几个小时的时间`
>
> `为了搞这个，自由时间我大概花了两个下午，四五个晚自习`
>
> `而且，我缺了一次微积分作业，翘了一次历史课，水了两节计算思维和新生教育......无数天一点多睡觉......我真的没那么多时间可挤了`
>
> ~~以及我真的没有中途心血来潮通宵学完了0基础入门python~~
>
> **其实还有很重要的一点：很多过程说实话我是失败了的，我已经花了极长的时间试了无数次错吸收了无数教训，最终只证明一件事：**
>
> **你32位就是不配！！！**
>
> `我会尽量把探索和失败的过程重现出来。`
>
> `不过讲真，我花了这么长时间试了这么多的错，得到的经验一定比那些64位毫无阻力做完我用几个晚上也搞不来的事情的同学多得多得多！！！！特别是关于硬件方面的！！！不虚`
>
> `害，xgg xjj都见的多了吧这种负面情绪，可谁想卖惨呢23333，但是超出预算的付出如果不宣泄出来的话人可能真的会心理出问题吧hhhh`
>
> `我也觉得废话太长了23333，下面开始~`

###  1、ubuntu 安装与使用

###### step1.了解情况后在google官网上下载安装vmware workstation~(早已被32位电脑的版本兼容问题搞到麻木……真的到处查)

嗯，截图如下(三四天前搞的，其实我也不记得我在哪里下载的2333，只记得当时我真的挣扎了好久好久)

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/1b24110ff8025f7f4.jpg" alt="1b24110ff8025f7f4.jpg" style="zoom:50%;" />

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/222222222.jpg" alt="222222222.jpg" style="zoom:50%;" />

刚开始去官网下的，但是好像要下载十年……

后来求助了一下导生，然后就知道了清华等学校有镜像源（听说我电以前也有…)

于是就下载安装呗

以上全程自己摸索，大概花了一个下午加半个晚上...从汉化到网络配置...后来我才在b站上看到全程的教程,一二十分钟就可以搞完...当时我想毁灭整个世界

一些历史记录拼接：（一部分，其实用网页打开看的也很多）

**损坏图片[请自动脑补一张有亿点长的b站历史记录拼接长图]**

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/B10DC92BFB270E82CC35ACA4E941A033.jpg" alt="B10DC92BFB270E82CC35ACA4E941A033.jpg" style="zoom:25%;" />

因为配置问题，第一个虚拟机宣布被弃，建了第二个

但是安装成功后还是很开心的(发了说说hhh)

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/30384260e8bf76d1e.png" alt="30384260e8bf76d1e.png" style="zoom:50%;" />

然后在 CSDN 上摸索，换了阿里源~

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/QQ20201015013103.jpg" alt="QQ20201015013103.jpg" style="zoom:25%;" />

非常抱歉截图很少（跪）

## 2、桌面美化

我太喜欢mac了，就搞了mac(太好看了吧！)

###### step1.全屏

这步操作时间有点久远了，说实话我真的不记得怎么做的了...只记得当时卡到显示比例啥的地方卡了很久（随意搜了一个背景）

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/4.jpg" alt="4.jpg" style="zoom:50%;" />

###### step2.背景主题图标字体等等的配置

主要参考了CSDN和b站上的教程，但是终端语法真的把我搞自闭了(看了看b站linux长达二十多个小时的教程时长，我咬着牙自己无限试错下去...)

大概试了七八个才搞好，我记得这个至少搞了两节晚自习和一次历史课(23333)

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/QQ20201015012551.jpg" alt="QQ20201015012551.jpg" style="zoom:25%;" />

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/3DBE9465ABA6B60598A76B02B7306730.jpg" alt="3DBE9465ABA6B60598A76B02B7306730.jpg" style="zoom:25%;" />

无法定位软件包，403 NOT FOUND，无法获得锁什么的，各种错试了个遍

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/5.jpg" alt="5.jpg" style="zoom:50%;" />

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/QQ202010150131239b553dd871b1a2b9.jpg" alt="QQ202010150131239b553dd871b1a2b9.jpg" style="zoom:25%;" />



<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/FAF7345EC273D334690B16A473840D83.jpg" alt="FAF7345EC273D334690B16A473840D83.jpg" style="zoom:25%;" />

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/E4A576C8BE4E107B9FDC8464B3C882B9.jpg" alt="E4A576C8BE4E107B9FDC8464B3C882B9.jpg" style="zoom:25%;" />

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/QQ20201015013423.jpg" alt="QQ20201015013423.jpg" style="zoom:25%;" />

最后知道下面那个玩意儿是dock，也花了我好长时间

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/QQ20201015012615.jpg" alt="QQ20201015012615.jpg" style="zoom:25%;" />

具体先安装工具啊啥的我就不赘述了

但是最终效果太喜人了吧：

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/QQ20201015011627.jpg" alt="QQ20201015011627.jpg" style="zoom:50%;" />

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/DE4A57196118906CBB93B9CE4391A556.jpg" alt="DE4A57196118906CBB93B9CE4391A556.jpg" style="zoom:50%;" />

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/925B547B9B47B3D92225E6F73D5971ED.jpg" alt="925B547B9B47B3D92225E6F73D5971ED.jpg" style="zoom:50%;" />

我重新爱上这世界了23333

## 3.装机必备软件下载(日常配置)

~~失败了，散了吧~~

下载了git,kazam什么的（在CSDN上查到了一些能下载的东西）

微信下载了一个多小时，从找版本到查怎么安装上

然后告诉我不能用...(谁事先能知道呢...)

对不起，我对deepin-wine 失去了兴趣，以后用树莓派装吧。(万念俱灰.jpg)

试了试找了找别的软件，x86着实把我搞吐了（大概花了两个晚上吧）

chrome 等等根本没有x86能用的版本

To sum up,我不把它当日常使用了，以后用可可爱爱的树莓派吧。

反正早晚是会用的/doge

一小部分截图

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/QQ20201015013021.jpg" alt="QQ20201015013021.jpg" style="zoom:25%;" />



<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/QQ2020101501313015179456eecc4e0a.jpg" alt="QQ2020101501313015179456eecc4e0a.jpg" style="zoom:25%;" />

（下图证明我试过23333）：

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/QQ20201015015619.png" alt="QQ20201015015619.png" style="zoom:25%;" />

当然这只是手机上的历史记录，电脑上估计比这多得多...

## 三、执行c语言代码

我去官网下载clion，结果需要jdk，然后我一查，我嘞个乖乖，  根本没x86的，淦！

对不起，我对配置IDE失去了兴趣。

其实再探索下去搞版本兼容问题已经毫无意义了

不过我win7上IDE还是有的

随便来贴一道简单的oj题吧，太难的我也做不来（随便找了个ide）：

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/QQ20201015021432.jpg" alt="QQ20201015021432.jpg" style="zoom: 80%;" />

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/QQ20201015021628.jpg" alt="QQ20201015021628.jpg" style="zoom:50%;" />

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/QQ20201015021631.jpg" alt="QQ20201015021631.jpg" style="zoom:50%;" />

只希望不要给我零分就好吧hhhhh

在这里再贴一个我们班级群里流行起来的狂奶大佬的代码23333：

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/QQ20201015022315.jpg" alt="QQ20201015022315.jpg" style="zoom:50%;" />

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/QQ20201015022321.jpg" alt="QQ20201015022321.jpg" style="zoom:50%;" />

/双手合十 /双手合十 /双手合十

## 四、写在最后

因为起步比较晚吧，针对各大工作室的学习大概持续了二十多天

这期间熬了太多太多的夜了

不停在试错，不停在试错

那么多日子都做了什么呢

挂了梯子科学上网，学了md

下载并学习了sai,ps,pr（学完是不可能学完的hhhhh）

收藏一堆ui设计网站闲了看看，下载了axure（搞完Linux 就学23333）

预习c语言，并且一夜肝完python基础

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/QQ20201015013155.jpg" alt="QQ20201015013155.jpg" style="zoom:50%;" />

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/QQ20201015013429.jpg" alt="QQ20201015013429.jpg" style="zoom:50%;" />

下载了git,github并看了一**小**部分教程hhhh

配置了一台虚拟机，对Linux有了与之前完全不一样的感受

但对我最重要的，应该还是对大量底层常识的恶补吧

当然还有一些社会小经验，比如找破解版软件，淘宝买软件会员，找脚本什么的hhhhh，之前完全不知道...

还有对搜索引擎强大性的深切感受...

（下图  日常23333）

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/QQ20201015013139.jpg" alt="QQ20201015013139.jpg" style="zoom: 25%;" />

记了许多笔记，了解了许许多多术语：

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/QQ20201015025627.jpg" alt="QQ20201015025627.jpg" style="zoom:25%;" />

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/8B18429F1AAB1361F3086CEBDDE131D9.jpg" alt="8B18429F1AAB1361F3086CEBDDE131D9.jpg" style="zoom: 50%;" />

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/QQ20201015025817.jpg" alt="QQ20201015025817.jpg" style="zoom: 25%;" />

只是觉得，虽然我费了这么大劲，但这只是恶补其他同学前几年已经做过的经验积累吧

从下载一个软件不知道怎么搞，一下子就搞一整个下午，连.exe都不知道是啥，甚至连操作系统都没概念，只知道window

到意识到国内许多软件的流氓性质，给电脑大清理，卸载了360全家桶、搜狗，下载了火绒、7-zip什么的

觉得自己懂的东西慢慢多起来了吧

之前被折磨那一段时间是真的自闭

又身兼学委，两科科代表，两科小组长

被佬骂过，崩溃过

真的很压抑

（还好春猪原声和aimer的陪伴让我保持仅存的人性2333333）

<img src="https://wpcos-1300629776.cos.ap-chengdu.myqcloud.com/Gallery/2020/10/15/2CF95709E39DDDB2D8E57176114D9C63.jpg" alt="2CF95709E39DDDB2D8E57176114D9C63.jpg" style="zoom:25%;" />

基础太薄，没法与身边的大佬相比

可我现在觉得

尽力就好

毕竟已经很累啦

不过以后会继续累下去的hhhh

凌晨四点多了......

咋说嘞，希望学长学姐能接纳我吧

这里是吴维熙哟！
