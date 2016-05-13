##iOS每日一读列表

##UIKit

1. [Understanding UIScrollView](http://oleb.net/blog/2014/04/understanding-uiscrollview/)。

	本文主要首先讲解了ScrollView frame 和 bounds，并讲解了ScrollView如何通过更改 bounds 达到滚动的效果，最后给出例子如何自己实现一个粗略的 ScrollView。

	注：文中附有短视频，所以较易懂。

	附：个人根据文中代码写的一个测试工程见：[文中代码示例](https://git.hz.netease.com/hzbaitianyu/BuildScrollView)

1. [为什么要同时设计UIView和CALayer](http://www.cocoachina.com/ios/20150828/13257.html). 本文较短，讲解了苹果为什么要拥有 CALayer和UIView两者来管理UI，文章以幽默风趣的方式从机制和策略分离的角度分析了CALayer和UIView各自的必要性以及苹果设计上考虑的周全性。通过阅读本文可以学习到苹果在设计UIView和CALayer时优秀的设计思想。

1. [Dynamic Table View Cell Height and Auto Layout](http://www.raywenderlich.com/73602/dynamic-table-view-cell-height-auto-layout)本文介绍了如何使用AutoLayout来做动态高度的TableViewCell

1. [iOS每日一读](http://ios.jobbole.com/83062/) 这篇文章主要介绍了自定义一个iOS控件，需要注意的方方面面，包括初始化、布局调整、事件处理、自定义视觉、不规则显示等等，虽然部分内容可能也也比较基础，但很多普适的知识点还是有必要多多了解的
1. 作者通过实现一个tableView，来让大家了解UI编程的一些基础内容和注意点[TableView实现](http://blog.jobbole.com/61101/)。还有一篇自定义控件的技巧和一些渲染机制，文章不长。[自定义控件](https://www.objc.io/issues/3-views/custom-controls/)

1. [导航栏那些事儿](http://www.jianshu.com/p/f797793d683f)介绍UINavigationBar 、 UINavigationItem 、UIButton、UIToolBar 、 UITabBar的区别；在storyboard如何添加navigation item

1. [使用Flexible实现手淘H5页面的终端适配](https://github.com/amfe/article/issues/17)。其中viewport的基础知识可以看这里[viewports剖析](http://www.w3cplus.com/css/viewports.html)

1. [一文让你彻底了解iOS字体相关知识](http://www.cnblogs.com/dsxniubility/p/4699352.html) 很基础实用的字体设置知识介绍。动态下载apple提供的中文字体可以阅读:[动态下载苹果提供的多种中文字体](http://blog.devtang.com/blog/2013/08/11/ios-asian-font-download-introduction/) 


#动画
[Creating Simple Animations with Facebook’s Pop Framework](http://www.appcoda.com/facebook-pop-framework-intro/)
介绍如何使用pop写property animation、spring animation、decay animation以及界面跳转动画。

1. [iOS每日一读](http://ios.jobbole.com/83062/) 这篇文章主要介绍了自定义一个iOS控件，需要注意的方方面面，包括初始化、布局调整、事件处理、自定义视觉、不规则显示等等，虽然部分内容可能也也比较基础，但很多普适的知识点还是有必要多多了解的

《关于UIImagePickerController的黑魔法》，作者根据需求定制相机的一些思路和小技巧，其中在获得notification name时还用了swizzling方法（这玩意儿真是可大用可小用），值得思考和学习，链接：http://www.jianshu.com/p/b82c58c9f2aa

[Interactive Animations](https://www.objc.io/issues/12-animations/interactive-animations/) ，我们常用的animation接口，设置animation之后，要么就一定要等到动画做完才响应用户交互或者添加新的动画，要么是强行移除animation再做这些事情，第二种会导致动画的不连续性。本文主要介绍
如何写出更加符合直觉的动画Interactive Animations，实现一个类似于iPhone的控制中心面板一些的效果，可以用手机感受下控制中心面板上的交互性动画效果。


##图片
###[移动端图片格式调研](http://blog.ibireme.com/2015/11/02/mobile_image_benchmark/)
移动端炫酷效果的实现，一般来说要么靠动画，要么靠图片，而流量耗费大部分都是图片产生的。合理的图片格式选用和优化可以节省带宽、提升视觉效果。这篇文章分析了主要几种图片格式的特点、性能（编解码、压缩比以及直观视觉感受，有精确的测试数据支撑）、参数调优，还有相关开源库的选择，值得推荐

##Persistent
[iOS中几种数据持久化方案](http://www.cocoachina.com/ios/20150720/12610.html)

介绍iOS常用的数据持久化方式，包括plist、preference、NSKeyedArchiver、SQLite、CoreData等，也介绍了封装SQLite的FMDB框架。当然，还有最基本的直接写文件方式，太简单了文章没有特意提

##Network
[IOS安全之HTTPS](http://www.cocoachina.com/ios/20150810/12947.html)。

如何打造一个安全的App？这是每一个移动开发者必须面对的问题。

本文先是介绍了HTTPS，然后举例NSURLConnection支持HTTPS的实现和使用AFNetworking来支持HTTPS。文中的几个外链也挺不错。

一篇关于TCP/UDP、HTTP和Socket的干货文章：[iOS的TCP/IP协议族剖析&&Socket](http://www.cocoachina.com/ios/20160223/15347.html)。对于这些网络知识的一些基础知识可以巩固一下。同时可以了解一下Socket的通信机制。算是一篇比较基础的文章


##优秀开源库
[AFNetworking2.0源码解析](http://blog.cnbang.net/tech/2320/)
一共是有三篇，大家最好是将这系列的文章都看完。
主要是作者对于AFNetworking 2.0源代码的解析与说明; 一方面有助于大家深入理解AFNetworking 2.0; 另一方面，也可以学习AFN作者对于OC的运用以及一些设计理念.

[ReactiveCocoa](http://benbeng.leanote.com/post/ReactiveCocoaTutorial-part1)
一个函数响应式编程（FRP）框架，本文是对其的入门介绍。

[浅析MagicalRecord](http://ddrccw.github.io/2014/05/19/a-brief-analysis-and-tips-on-magialrecord/)
是除了常用哪几种的数据持久化存储存储手段(Plist文件，SQLite，FMDB等等)之外，的MagicalRecord也是一个不错的选择，它是对coreData做了更易用的封装，这篇文章对其做了较好的剖析

[DTCoreText 数据篇](http://blog.cnbang.net/tech/2630/) [DTCoreText 渲染篇](DTCoreText源码解析 渲染篇) DTCoreText是个开源的iOS富文本组件，它可以解析HTML与CSS最终用CoreText绘制出来，通常用于在一些需要显示富文本的场景下代替低性能的UIWebView.这两篇循循渐进对其设计实现思路进行了剖析

##Map&Location
解决地图上大头针数量多而导致的性能下降的问题。
当地图上含有上百个大头针时，不但会使得CPU消耗巨大，也会导致大头针过于拥挤。
这两篇文章讲述了各自的解决方案。一种消耗比较小的方法是使用聚类的方案，数据结构使用了四叉树，根据地图的缩放比例，不断调整应该显示的大头针。两篇文章都给出了源码和实例。
https://infinum.co/the-capsized-eight/articles/a-blazingly-fast-open-source-algorithm-for-poi-clustering-on-ios
http://applidium.com/en/news/too_many_pins_on_your_map/

##Core Animation&Render
[Getting Pixels onto the Screen](http://www.objc.io/issues/3-views/moving-pixels-onto-the-screen/) 非常不错的科普文章，讲解了iOS下一个像素如何最终渲染出来。里面包含了iOS渲染方面各种概念，甚至包括png,jpeg的选择。

-------------------
[designing-for-ios-taming-uibutton](https://robots.thoughtbot.com/designing-for-ios-taming-uibutton)
讲解了怎么渲染一个按钮的背景的四种方法：

1. resizeable image（最佳选择，性能最高）
1. 大的背景图(性能较次，耗内存)
1. 使用core graphics绘制（使用CPU渲染，性能更差）
1. 使用layer组合出来（性能更差，存在离屏渲染，实际上也是要生成一个大图，好处是可以定义transition动画，要绘制多个Layer，存在过度绘制<overdrawn>）

[文章评论：UIKit团队成员](https://news.ycombinator.com/item?id=4645585)


[一款Loading动画的实现思路](http://www.jianshu.com/p/1c6a2de68753)    
作者非常细致的描述了一款加载动画的实现思路与过程，讲解得非常细致，描述如何将复杂动画拆解成为简单任务一步步实现；系列文章一共有三篇，可以都看看。

##CoreSpotlight
[IOS9应用内搜索](http://www.cnblogs.com/CocoonJin/p/4703366.html)在iOS9之前我们只能使用Spotlight来搜索应用名称来打开指定App。在iOS9以后Apple允许开发者设置应用中任意内容可以被Spotlight索引。本文介绍了iOS 9之应用内搜索(CoreSpotlight）的简单实现。
[更多IOS9适配相关](https://www.shinobicontrols.com/blog/ios9-day-by-day-index)。
##UniversalLink
[IOS9通用链接使用](https://blog.branch.io/how-to-setup-universal-links-to-deep-link-on-apple-ios-9)IOS9推出了通用链接功能，通过唯一的网址, 就可以链接一个特定的视图到你的 APP 里面, 不需要特别的 schema。本文详细介绍了介绍了通用链接的使用。

##Runtime
[Associated-Objects](http://kingscocoa.com/tutorials/associated-objects/)
 描述的是runtime机制的associated-objects的用法，并且对于associated-objects用法的一些优化措施。在category的时候经常会使用到。这篇文章对associated-objects用法描述属于层层优化的过程。

[Autorelease Pool的实现原理](http://blog.leichunfeng.com/blog/2015/05/31/objective-c-autorelease-pool-implementation-principle/)
文章剖析了Autorelease Pool的实现原理，基本上，pool page存储了Autorelease Pool创建与释放的信息，其结构用栈+双向链表的结构来实现，创建pool并给对象发送Autorelease消息可以看成是入栈，pool drain可以看做是将其中元素出栈。
系统的pool的创建与销毁和runloop有关，自己写的@autorelease{}在是作用域结束后立即释放的。

[从C的伪代码到汇编,动手实现objc_msgSend](http://www.cocoachina.com/ios/20150812/12992.html)
对runtime有一定认识之后，可以考虑下如何能实现出objc_msgSend这个oc中消息机制的幕后功臣了


[Dive into Category](http://www.cocoachina.com/ios/20150330/11427.html)
Category是Objective-C语言很重要也很实用的一个特性，能够极大地提高开发语言的灵活性。本文是作者学习Objective-C的runtime源码时整理所成，主要剖析了category在runtime层的实现原理以及和category相关的方方面面

[Hook - Swizzling](http://blog.csdn.net/u014599371/article/details/43563987)
在没有一个类的实现源码的情况下，想改变其中一个方法的实现，除了继承它重写、和借助类别重名方法暴力抢先之外，由于 **Runtime** 提供的动态特性，我们可以 **Hook** 一个方法进行定制性操作。本文介绍了 **Hook** 方案 **Swizzling** 的基本使用以及使用时需要注意的事项。使用 **Hook** 可能需要对运行时有一定了解，此处另推荐一篇跟运行时有关的blog [What is a meta-class](http://www.cocoawithlove.com/2010/01/what-is-meta-class-in-objective-c.html) ，文章简单明了的解释了 object、class & meta-class 的关系。

[_objc_msgForward函数是做什么的，直接调用它将会发生什么？](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01%E3%80%8A%E6%8B%9B%E8%81%98%E4%B8%80%E4%B8%AA%E9%9D%A0%E8%B0%B1%E7%9A%84iOS%E3%80%8B%E9%9D%A2%E8%AF%95%E9%A2%98%E5%8F%82%E8%80%83%E7%AD%94%E6%A1%88/%E3%80%8A%E6%8B%9B%E8%81%98%E4%B8%80%E4%B8%AA%E9%9D%A0%E8%B0%B1%E7%9A%84iOS%E3%80%8B%E9%9D%A2%E8%AF%95%E9%A2%98%E5%8F%82%E8%80%83%E7%AD%94%E6%A1%88%EF%BC%88%E4%B8%8B%EF%BC%89.md#25-_objc_msgforward%E5%87%BD%E6%95%B0%E6%98%AF%E5%81%9A%E4%BB%80%E4%B9%88%E7%9A%84%E7%9B%B4%E6%8E%A5%E8%B0%83%E7%94%A8%E5%AE%83%E5%B0%86%E4%BC%9A%E5%8F%91%E7%94%9F%E4%BB%80%E4%B9%88)这是系列IOS面试题中的一道，为大家提供了新的调试技巧，可以打印运行时发送的所有消息。通过运行时的日志，可以清晰地查看消息转发的流程。这为我们提供了新的消息转发选择：借助`_objc_msgForward`来实现消息转发，比如LDAOPAspect就是通过将方法的IMP指针设置为`_objc_msgForward`来完成消息转发。
 
[Objective-C 方法缓存](http://tech.meituan.com/DiveIntoMethodCache.html)
美团团队对OC源码进行了研究并输出了这篇技术文章分享，本文讲了Objective-C 的方法缓存机制，从最简单的方法调用开始，逐步深入runtime，详细介绍了OC中方法的缓存。

##框架
NSNotification相关文章

推荐两篇关联的文章，

[NSNotificationCenter](http://southpeak.github.io/blog/2015/03/20/nsnotificationcenter/)

[Notification与多线程](http://southpeak.github.io/blog/2015/03/14/nsnotificationyu-duo-xian-cheng/)

作者主要是整理了一下 NSNotificatonCenter的使用以及需要注意的问题，尤其是与多线程下使用相关的一些问题，对掌握NSNotification还是比较有帮助的。


##语言
这是一系列文章，主题就是“手把手教你做一个 C 语言编译器”！
虽然没有好好学过《编译原理》这门课，但不妨碍我们再次造轮子的乐趣。
[手把手教你做一个 C 语言编译器](http://blog.jobbole.com/97332/)

##汇编
[iOS Assembly Tutorial: Understanding ARM](http://www.raywenderlich.com/37181/ios-assembly-tutorial)浅显易懂的ARM汇编介绍文档

[Mach-O 可执行文件](https://www.objc.io/issues/6-build-tools/mach-o-executables/)
曾经在MAM开发过程中遇到了如何在IOS中拦截C函数的调用的问题，最终的解决方案是修改运行时符号表的指针，关键部分之一就是查找可执行文件中的函数指针；Router也使用可执行文件缓存了一些信息，提高了程序启动速度；所以了解可执行文件的结构对于一些AOP编程和性能优化需求是非常有效果的。

-------------------


##架构

[iOS应用架构谈 view层的组织和调用方案](http://casatwy.com/iosying-yong-jia-gou-tan-viewceng-de-zu-zhi-he-diao-yong-fang-an.html)
作者现在在天猫做iOS应用架构方面的工作，之前是安居客的主程。这篇文章主要是谈了一下iOS应用在view层应该如何架构和组织代码；以及如何在现有基础上去逐步改进优化架构，其设计思想我觉得还是很有价值的，可以慢慢体会。除了这一篇之外，他博客上其他几篇谈架构的文章都值得看一看，文章下面的讨论也都还比较有意思，值得一看。

[被误解的 MVC 和被神化的 MVVM](http://blog.devtang.com/blog/2015/11/02/mvc-and-mvvm/)            
唐巧最新的文章，主要是介绍了一下作者自己对MVC和MVVM的一些理解，以及对应用新技术的一些看法，并且给出一些实际开发工程中的建议。其实，相关的道理都是浅显易懂，但是在实际的开发过程中，要使得架构层次清晰、便于维护和扩展又不是一件容易的事情，大家可以从这篇文章中汲取对自己有益的部分，并在实际开发过程中慢慢体会并且逐步应用一些实用的技巧。

[iOS Design Patterns](http://www.raywenderlich.com/46988/ios-design-patterns)         
介绍iOS开发中常用的设计模式以及对应实现方法，包括单例模式，MVC模式，代理模式，外观模式，观察者模式，装饰模式，备忘录模式和命令模式等等；对于学习和理解设计模式以及如何在iOS开发中应用都比较有帮助。

[猿题库 iOS 客户端架构设计](http://mp.weixin.qq.com/s?__biz=MjM5NTIyNTUyMQ==&mid=444322139&idx=1&sn=c7bef4d439f46ee539aa76d612023d43&scene=23&srcid=1230RYRzNotU9iTZKvt7ksFW#rd&ADUIN=502332019&ADSESSION=1451480917&ADTAG=CLIENT.QQ.5425_.0&ADPUBNO=26509)   
作者是猿题库的iOS开发者, 详细介绍了猿题库客户端架构的设计和思考，当然，也有大量的代码示例。作者Lancy 引入了一个名为 Data Controller 的层级为 View Controller 瘦身，并且借鉴了 MVVM 的思想来将界面与底层解耦, 而不是单纯的往MVC和MVVM上去套。补充一句，这篇文章我并没有看到在作者自己的博客上发遍，而是直接投稿在唐巧维护的"iOS开发"微信公众号上，大家也可以关注这个公众号，里面不时会有一些非常好的文章。

[iOS应用架构谈 组件化方案](http://casatwy.com/iOS-Modulization.html )前面大家可能都看过Limboy分享的蘑菇街组件化方案，该篇文章是作者对于蘑菇街组件化方案分析，并且提供自己的组件化方案。
这是Limboy的蘑菇街组件化之路 [蘑菇街组件化之路](http://limboy.me/ios/2016/03/10/mgj-components.html)  
这是Limboy回应上面文章的第二篇文章[蘑菇街组件化之路-续](http://limboy.me/ios/2016/03/14/mgj-components-continued.html)

##统计打点
[IOS项目中统计打点的一种方案](http://limboy.me/ios/2015/09/09/ios-analytics.html)

在IOS开发中常常用到统计打点，通常是与具体的业务逻辑代码混杂在一起（云阅读是如此），本文提供了统计打点的一种思路，值得在项目开发中借鉴。

##APP
[由App启动说起](http://www.cocoachina.com/ios/20160118/15019.html)

“你是谁？从哪里来？到哪里去？”，这三个富有哲学气息的问题，是每一个人在不断解答的问题。我们Code，Build，Run，一个活生生的App跃然方寸屏上，这一切是如何发生的？从用户点击App到执行main函数这短短的瞬间发生了多少事呢？探寻App的启动新生，可以帮助我们更了解App开发本身。

##Xcode
Xcode制作动态库，iOS加载动态库
[Dynamic linking on iOS](http://ddeville.me/2014/04/dynamic-linking/)

[xCode6制作动态及静态Framework](http://years.im/Home/Article/detail/id/52.html)

[WWDC2014之iOS使用动态库](http://foggry.com/blog/2014/06/12/wwdc2014zhi-iosshi-yong-dong-tai-ku/)


[Xcode断点魔法](https://www.bignerdranch.com/blog/xcode-breakpoint-wizardry/)
每个开发者都需要花大量的精力来调试代码，要是掌握了调试技巧，就能够达到事半功倍的效果。  
本文细致地介绍了Xcode的断点技巧：
1. 介绍了Xcode断点的使用方式，在断点处执行lldb命令（lldb命令进阶：[与调试器共舞](http://objccn.io/issue-19-2/)），
2. 使用 Symbol 断点可以方便地用类名，方法名设置断点，
3. 使用 Watchpoints 观察变量的修改

[Xcode7 插件制作入门](http://www.cocoachina.com/ios/20160229/15476.html)
平时用了很多xcode插件，使我们的工作效率成吨的提高，如果自己想要制作一个插件改怎么办呢，本文介绍了xcode7下插件的制作，可做简单入门之用。

[Runtime Code Injection for Objective-C & Swift](https://github.com/johnno1962/injectionforxcode)
个Xcode插件,不需要重新运行整个应用，在运行时就能将修改过的代码编译运行，节省调试时间。效果和Swift的Playground类似，可以实时地看到敲入代码的效果，优点是支持Objective-C。基本原理是通过插件工程编译修改后的代码，再动态链接插件工程的二进制文件，通过重新加载页面刷新当前页面。

##Crash

[iOS崩溃调试的使用和技巧总结](http://www.cocoachina.com/ios/20151218/14748.html):在iOS开发调试过程中以及上线之后，程序经常会出现崩溃的问题。简单的崩溃还好说，复杂的崩溃就需要我们通过解析Crash文件来分析了,本文总结一些崩溃调试的使用和技巧。

[漫谈iOS Crash收集框架](http://www.cocoachina.com/ios/20150701/12301.html)
作者简单地讲解了 IOS 中 三种类型的Crash，给开发者展示 Crash 收集框架的原理，结尾引用的野指针 Crash等问题的文章非常精彩。

-------------------

##关于学习：
[十年学会编程](http://daiyuwen.freeshell.org/gb/misc/21-days-cn.html)  学习这事对于现在的技术人员太重要了，这篇文章主要讲  程序员  什么值得学，什么值得投入时间。 

[如何教会女朋友编程](http://article.yeeyan.org/view/552155/464601)里面一句话很赞成：思考问题的角度比得上80点IQ值。 一名专业的开发者在某种程度上也是一名专业的老师，因为我们的工作要求我们不断向别人解释我们做的东西。我们不得不将自己代入读者的角色，从而使代码更加通俗易懂。当代码不起作用时我们还不得不解释我们做了什么，同时我们还要在实习生成为大牛的路上点拨几句。
我们所有的工作内容就是把复杂的东西变得简单


##多线程相关

1. [How To Use NSOperations and NSOperationQueues](http://www.raywenderlich.com/19788/how-to-use-nsoperations-and-nsoperationqueues)

很多app的首页都是tableview加载一组列表名称，再加载名称所对应的资源如图片等，本文以这个基本流程为基础，介绍如何使用NSOperation和OperationQueue来提升用户体验，此外还介绍了一些细节上的优化，比如在用户手放开且滑动结束之后再进行网络请求等，推荐阅读。

1. [五个案例让你明白GCD死锁](http://ios.jobbole.com/82622/)

1. [深入理解RunLoop](http://blog.ibireme.com/2015/05/18/runloop/)这篇文章将从 CFRunLoop 的源码入手，介绍 RunLoop 的概念以及底层实现原理。之后会介绍一下在 iOS 中，苹果是如何利用 RunLoop 实现自动释放池、延迟回调、触摸事件、屏幕刷新等功能的。

1. [如何打造自己的dispatch_queue](https://mikeash.com/pyblog/friday-qa-2015-09-04-lets-build-dispatch_queue.html)
GCD是OC很好用的一个特性，但简介优雅地的dispatch_sync/dispatch_async是怎么实现的，又是怎样在dispatch_queue上执行的？这篇文章就引导我们如何去实现自己的dispatch_queue，看看其背后是有什么魔法
1.	[GCD的dispatch source](http://blog.afantree.com/gcd/ios-gcd-learning-dispatch-sources.html)  
本文谈到如何使用GCD的dispatch source功能来监视文件描述符、计时器、联结的用户事件以及其他类似的行为。全面直观地展示了GCD在事件处理上的强大和接口设计的清晰

##基本原理

[从输入 URL 到页面加载完成的过程中都发生了什么事情？](http://fex.baidu.com/blog/2014/05/what-happen/)
来自某位前端大牛的面试题目，看似简单，发散开来，却涉及了从设备硬件到网络介质到网络拓扑到后端处理再到HTTP协议再到浏览器再到屏幕渲染的方方面面，可以把计算机网络和计算机组成原理都复习一遍了

[相机工作原理](http://objccn.io/issue-21-1/)讲解了相机成像的基本原理，并分别介绍了快门速度，感光度 (ISO)，光圈对成像的影响，让你更懂你的相机。

[URL Schemes](http://iosdevelopertips.com/cocoa/launching-your-own-application-via-a-custom-url-scheme.html) iOS中应用跳转需要使用到URL Schemes,本文讲解了如何定制跳转信息，既可以从浏览器启动应用也可以通过其它APP启动。  （自己做demo的时候建议真机测试，模拟器我测的时候两个应用之间跳转会失败）

[__block的原理](http://chun.tips/blog/2014/11/13/hei-mu-bei-hou-de-blockxiu-shi-fu/)

##算法
[25匹马](http://hxraid.iteye.com/blog/662643)正向选择的同时可以减少下次选择的范围，加快算法速度。 
 
[动态规划：从新手到专家](http://www.hawstein.com/posts/dp-novice-to-advanced.html)这次推荐与iOS无关，推荐的是算法中的动态规划，讲得比较细致，由小及大的例子，比较容易让人清楚动态规划的概念。虽然是翻译但作者加入了自己的见解。 如果对动态规划不是很了解的看完后都可以有一定的掌握（当然，熟练还是靠多次编程）

##安全
[iOS App Security and Analysis: Part 1/2](http://www.raywenderlich.com/45645/ios-app-security-analysis-part-1)

[iOS App Security and Analysis: Part 2/2](http://www.raywenderlich.com/46223/ios-app-security-analysis-part-2)

iOS安全编程常见注意事项，常见简单攻击方式以及防御方式。


-------------------

##宏
[宏定义的黑魔法](http://onevcat.com/2014/01/black-magic-in-macro/)

宏可以优化编译，节省工作量，让代码简洁好用。在C系开发中举足若轻，这篇文章由浅到深地介绍了宏的定义和常用的宏定义。本文看点：

+	定义一个工具宏存在的挑战
+	学习NSLog的定义
+	定义不会重名的宏
+	宏定义的一些技巧，如while循环

##Hybrid
[Best Of Both Worlds: Mixing HTML5 And Native Code](http://www.smashingmagazine.com/2013/10/best-of-both-worlds-mixing-html5-native-code/)本文理性的介绍了app中分别使用web和native优缺点，（web的热更新能力，动画和排版的灵活性；native的设备访问权限，流畅的用户体验，安全性）不偏不倚，提倡开发人员选择合适的技术来解决实际的问题。文中以示例展示了js与oc的互操作，从webview中url到native页面的跳转也是这个方式。另外，介绍了在使用hybrid技术时应该注意一些点。

[聊聊移动端跨平台开发的各种技术](http://fex.baidu.com/blog/2015/05/cross-mobile/) 本文介绍了主流的移动端跨平台的解决方案，涉及的面比较广，对我们后续做跨平台开发的一些调研有一定的指导作用。

##[Toll-free bridging介绍](https://mleasyzhuzhiqiang.github.io/)

这篇文章完整地展示了Toll-free bridging的实现原理，桥接，能够让开发者在OC和C之间自由地切换。例如CFReadStreamRef和NSInputStream等。这篇文章以看源代码的方式分析CoreFoundation和UIKit如何实现Toll-free bridging，可以提高开发者对ObjC对象模型的理解。


##设计模式

[iOS中常用设计模式](http://ios.jobbole.com/55505/) iOS开发中灰碰到各种设计模式的应用，比如监听者模式、委托模式、单例模式、工厂模式、MVC等等，那么这篇文章就主要以监听者模式做了较为详细的分析，包括Notification和KVO等，并做了一些改进的探索


------

##性能

###[iOS实时卡顿监控](http://www.tanhao.me/code/151113.html/index.html)
本文深入分析NSRunLoop，通过监控NSRunLoop状态，达到量化卡顿的目的。

## 工作流程
[Git 工作流程](http://www.ruanyifeng.com/blog/2015/12/git-workflow.html) 本文简单介绍了基于Git的三种广泛使用的工作流程，对于后续我们规范工作流程有一定的参考价值。

[JSPatch开源经验分享](http://mp.weixin.qq.com/s?__biz=MzA3ODg4MDk0Ng==&mid=403063229&idx=1&sn=34651b982e211ae64742913026d459b0&scene=0) JSPatch算是一个很知名的开源库了，我们可以学习一下别人是怎么做开源的，尤其是“ [面临的问题 - 业界解决方案 - 他们的缺陷 - 我的项目的优势 - 实现]”这个推广的思路我们可以借鉴一下。

## 网络

[HTTP 2.0的那些事](http://mrpeak.cn/blog/http2/)

作者介绍了HTTP2.0协议相关的一些知识，包括HTTP1.1协议存在的一些问题、过去的解决方案、HTTP2.0的设计思想以及HTTP2.0, SPDY等的优缺点都作了相应的介绍，并且也介绍了移动端对于HTTP/2以及SPDY相关的支持状况，对于大家了解网络请求的性能优化有很好的帮助。


## Swift
[Swift中的设计模式](http://www.infoq.com/cn/articles/design-patterns-in-swift)

这篇文章讨论并展示了设计模式在现代编程语言背景下的变化：要么被语言特性更好的代替了；要么变得更为简单了。作者使用Swift语言演示了5个设计模式和新的语言特性之间的关系。这5个设计模式和语言特性分别是：高阶函数和命令模式，一等函数和策略模式，柯里化函数和抽象工厂模式，扩展和适配器模式，运算符重载和解释器模式。

# Objective-C
[Objective C类方法load和initialize的区别](http://blog.iderzheng.com/objective-c-load-vs-initialize/)

# iOS安全
[非越狱平台进行“越狱”开发](http://mp.weixin.qq.com/s?__biz=MzI5MDIwNjc5Mw==&mid=402995734&idx=1&sn=567a479b0b05adb849f48a1cf924a7bd#rd)

主要讲解如何通过逆向分析，找到应用关键代码，然后编写dylib注入，最后运行到非越狱机器上的整个流程
