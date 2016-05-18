##Android每日一读列表

##网络相关

>20150813

* [网络库组合 okHttp、volley和gson](https://medium.com/android-news/android-networking-i-okhttp-volley-and-gson-72004efff196  )

这是Android网络开发库系列的第一篇，介绍了okHttp、volley和gson的组合，使网络请求更加简单、高效，不足之处是各部分的介绍相对简单，内容过少，不过给出了很多链接，感兴趣的同学可以逐渐深入学习。

>20150915

* [FlatBuffers的基础知识](http://www.iteye.com/news/30906 )

《开源、高效、跨平台：深剖Google FlatBuffers工作原理》几天前，Facebook宣布，其Android应用程序大幅提升了数据处理性能。这是由于几乎在全部应用程序中放弃了JSON数据格式，用FlatBuffers取而代之了.

>20150916

* [Android Https相关完全解析 当OkHttp遇到Https](http://blog.csdn.net/lmj623565791/article/details/48129405)  

okhttp默认情况下是支持https协议的网站的，不过要注意的是，支持的https的网站基本都是CA机构颁发的证书，默认情况下是可以信任的。我们今天要说的是自签名的网站。部分开发者app与自己服务端交互的时候可能也会遇到自签名证书的。甚至在开发安全级别很高的app时，需要用到双向证书的验证。
文章详细介绍了使用OkHttp访问自签名网站，以及进行双向证书验证的方法

>20151015

* [Android微信智能心跳方案](https://mp.weixin.qq.com/s?__biz=MzAwNDY1ODY2OQ==&mid=207243549&idx=1&sn=4ebe4beb8123f1b5ab58810ac8bc5994)  

微信开发工程师统计的各家推送的心跳时长和不同地区、不同网络的策略，包括What’s app、Line等，同时也讲解了采用这些策略的一些原因。讲的不深入，属于科普文。

>20160303

* [OkHttp缓存机制](http://www.schibsted.pl/2016/02/hood-okhttps-cache/)

OkHttp一个很好的特点就是它的缓存机制。在这篇文章走通了OkHttp缓存相关的步骤，并解释了它是如何工作。

>20160322

* [RxJava 与 Retrofit 结合的最佳实践](http://gank.io/post/56e80c2c677659311bed9841)

RxJava如何与Retrofit结合


##UI使用相关

>20150814

* [为什么你应该抛弃fragment？](https://corner.squareup.com/2014/10/advocating-against-android-fragments.html )

fragment最初的目的是用于平板的兼容，但仅作为一个view的容器，将fragment引入你的app会带来：

+ 1：混乱的生命周期；
+ 2:fragment事务的引入导致难以调试；
+ 3：fragment在架构中定位模糊

本文推荐替代fragment的方案是通过view/presenters将一个view容器组织起来，类似微mvp了

除了本文中推荐的Mortar库，square还开源了另一个Flow库，将两者一起使用也可以很好的替代fragment，有兴趣的同学可以扩展阅读：

https://www.bignerdranch.com/blog/an-investigation-into-flow-and-mortar/

>20150818

* [RecyclerView的相关使用方法](http://www.grokkingandroid.com/first-glance-androids-recyclerview/)

关于recyclerview，推荐理由：写的很全面，用法基本都覆盖到了， 包括Adapter、ViewHolder、LayoutManager以及动画（ItemAnimator）。
缺点：比较细，比较基础。

>20150914

* [Google推荐的图片加载库Glide介绍](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/0327/2650.html)

描述的是谷歌发布一个名叫 Glide 的图片加载库，并将它和Picasso在多方便进行了对比：Glide加载图像以及磁盘缓存的方式都要优于Picasso，速度更快，并且Glide更有利于减少OutOfMemoryError的发生，GIF动画是Glide的杀手锏。不过Picasso的图片质量更高。

其他相关资料：[Glide使用方法
](http://blog.csdn.net/fandong12388/article/details/46372255)

>20150923

* [Android机型适配之痛](http://www.csdn.net/article/2015-09-08/2825645/3)

Android机型适配的各种问题。
由于Android的碎片化严重，造成了Android适配的困难，作者从实际的适配中举例提到了一些在适配中可能遇到的普遍和奇葩的问题，喷了一下各大厂商。

>20160215

* [Android AutoLayout全新的适配方式 堪称适配终结者](http://blog.csdn.net/lmj623565791/article/details/49990941)

GitHub地址：https://github.com/hongyangAndroid/AndroidAutoLayout
Android屏幕适配方案，直接填写设计图上的像素尺寸即可完成适配（内部会进行百分比化处理）。最大幅度解决适配问题，并且最大化方便开发者。不用去想取多少dp，不用去写多个dimens。。。

>20150926

* 使用曲线的动态显示来达到一些炫酷的效果

	[三次贝塞尔曲线练习之弹性的圆](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/0915/3457.html): 使用三次贝塞尔定义5种中间状态，由此交给系统差值得到一个动态弹性的效果，简单有效

	[使用DashPathEffect绘制一条动画曲线](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/0907/3429.html): 使用DashPathEffect绘制曲线，并给出一个案例，通过PathEffect来实现动态的画线的效果。仅在使用层面上能，给了我们案例，能通过现有的矢量定义图形的方式创建一些比较吸引人的动态效果

>20160111

* [WebView上传文件的那些坑](http://blog.saymagic.cn/2015/11/08/webview-upload.html)

比较详细的讲解了使用 `WebView` 上传文件时，客户端需要做的配合，并且对于代码混淆和 sdk 版本的不同可能需要做的适配。虽然我们平常可能不太会使用 `WebView` 上传文件，但如果碰到的话，可以看下这篇文章，少走些弯路

> 20160218

* [谈谈App混合开发](http://bxbxbai.gitcafe.io/2015/08/16/talk-about-bybird-app/)

以网易云音乐、微信、Cordova为例，讲解了 `html` 和 `Native` 交互开发 app 的几种封装实现方式。对于我们后面的工程开发可能有一定的借鉴作用。

> 20160203

* [掌握Coordinator Layout](http://mp.weixin.qq.com/s?__biz=MzAwMDczNDY0MA==&mid=401949588&idx=1&sn=bbadcb285af31306403eaf286c23e94a&scene=5&srcid=0202DIk5CCP4pBJ0vqihw4ZL#rd)

在Google I/O 15上Google发布了新的支持库，包括几个类似于ViewGroup 的控件，如 AppbarLayout,CollapsingToolbarLayout 和 CoordinatorLayout。
这些ViewGroups控件提供了非常强大的功能，能够轻松做出很酷炫的效果。本文有详细的图文使用说明。


> 20160317

* [Android 中 RelativeLayout 和 LinearLayout 性能分析](http://gold.xitu.io/entry/56e8dd841ea4930055250fc5)

在用IDE创建新的Activity时，Google给开发者默认新建了个RelativeLayout，而google自己却在当前窗口的顶级View——DecorView中偷偷用了个LinearLayout，到底谁的性能更高，开发者该怎么选择呢？本文对这两种布局的原理和效率进行了详细分析。

>20160419

*[Android Bottom navigation 规范一](http://androidperformance.com/2016/04/05/android-bottom-bar-1.html) 和[Android Bottom navigation 规范二](http://androidperformance.com/2016/04/05/android-bottom-bar-2.html)

随着Bottom navigation组件的发布，android 官方也更新了一个新的设计规范，所谓设计规范就是告诉开发者和设计师要如何去设计和使用某一个组件。文章介绍了低栏设计规范的演化过程以及Bottom navigation组件的使用规范。
 附上看到的一个[团队博客推荐(阿里，美团，IBM和腾讯)](http://www.trinea.cn/android/internal-technical-community-blog/)

>20160517

google新开源了flexBox控件，在android端实现类似css前端Flexbox布局的开源项目，https://github.com/google/flexbox-layout
下文是stylingandroid是对各种布局约束的介绍
https://blog.stylingandroid.com/flexboxlayout-part-1/

##UI显示优化相关

>20150817

* [Android中文本显示的一个优化](http://instagram-engineering.tumblr.com/post/114508858967/improving-comment-rendering-on-android)

对于内容较多的复杂文本的显示，往往会在measuring和drawing中花费较多的时间，尤其是对可滚动的页面当中，会造成页面滚动卡顿的现象
本文推荐使用使用text.Layout对显示结果缓存，来极大的提高本文显示的效率。
本文不足之处是内容不多，且针对性强，对显示优化感兴趣的同学，可以看些其他的资料

>20150902

* [高斯模糊效果实现方案及性能对比](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/0831/3389.html)

对于移动端的图片模糊处理，该文提出了3中处理办法，RenderScript，FastBlur和AdvancedFastBlur。通过试验对比性能，发现AdvancedFastBlur可以在17ms（大概一帧的绘制时间）内完成，避免了应用的卡顿。AdvancedFastBlur采用了首先缩放图片，降低清晰度，后采用模糊的方式，极大缩减了运算时间，同时并没有对效果造成多少影响。因为缩放图片的尺寸比例是可以程序控制，所以使用者可以对于不同大小的图片采用不同的缩放比例。
本文不足之处是并没有进一步介绍RenderScript和FastBlur的内容，提到GPUs和CPUs的并行处理，但完全没有细讲。

>20151027

* [Android App性能评测与调优-内存与流畅度](http://bugly.qq.com/blog/?p=249)

从内存、UI流畅度、IO三个方面讲解了对APP性能的影响，分享风格偏重于内容深入浅出、提炼深刻、课件形象、案例丰富、实战经验强。

>20160308

* [LeakCanary](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/0511/2861.html) 和 [BlockCanary](http://blog.zhaiyifan.cn/2016/01/16/BlockCanaryTransparentPerformanceMonitor/)

2 款常用的工具，分别用来检测内存泄露和找出 UI 卡顿的原因。这里 BlockCanary 的设计思想值得我们借鉴，根据主线程的消息队列处理机制入手，设计了这个 UI 检测工具。
##UI事件相关

##本地存储相关

##图片显示和内存控制相关

>20150907

* [Solving the Android image loading problem: Volley vs Picasso](https://www.bignerdranch.com/blog/solving-the-android-image-loading-problem-volley-vs-picasso/)

Volley和Picasso是Google IO大会上推荐的库，本文从图片加载的角度对两个库进行比较，分析了两个库各自的优缺点。严格来说，Volley并不是专注图片加载的库，而对于主流专注图片加载的库Picasso、Glide、ImageLoader和Fresco之间的比较也存在很多讨论，有兴趣的同学可以了解下。

相关讨论：

Picasso v/s Imageloader v/s Fresco vs Glide

http://stackoverflow.com/questions/29363321/picasso-v-s-imageloader-v-s-fresco-vs-glide

Square Picasso vs Universal Image Loader

http://stackoverflow.com/questions/19995007/local-image-caching-solution-for-android-square-picasso-vs-universal-image-load


>20151013

* [Android 内存泄露一](https://www.zybuluo.com/linux1s1s/note/88606)
* [Android 内存泄露二](https://www.zybuluo.com/linux1s1s/note/88621)

分别讲述了Handler和Thread在使用过程中，可能造成内存泄露的原因和解决办法，讲解的很清楚；缺点是内容还不够全面，其他可能的情况并没有分析

>20151020

*[Android GC 那点事](http://mp.weixin.qq.com/s?__biz=MzI1MTA1MzM2Nw==&mid=400021278&idx=1&sn=0e971807eb0e9dcc1a81853189a092f3&scene=0#rd)

文章主要对Dalvik虚拟机和ART的内存分配和回收机制进行了分析对比，图文讲解，讲的还不错呢。

>20151029

* [Android内存分析一](https://www.zybuluo.com/linux1s1s/note/88636)
* [Android内存分析二](https://www.zybuluo.com/linux1s1s/note/88686)
* [Android 字体内存泄露](https://www.zybuluo.com/linux1s1s/note/139297)

讲了内存分析工具和视图工具，另外提到了使用字体文件可能造成内存泄露的问题。内容简单，但比较实用

>20160127
* [Android开发中各种常见的内存泄露总结](https://yq.aliyun.com/articles/3009?spm=5176.100240.searchblog.31.oDWxG1)这些内存泄露都挺常见的，通过咱们的规范，部分的泄露场景可以避免掉，文中做了一个总结，后面通过工具分析的部分应该被发过很多次了。

>20151023  

[Android内存优化之OOM](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/0920/3478.html)  
Android的内存优化是性能优化中很重要的一部分，而避免OOM又是内存优化中比较核心的一点。这是一篇关于内存优化中如何避免OOM的总结性概要文章，内容大多都是和OOM有关的实践总结概要。

>20151026  

[Android UI：机智的远程动态更新策略](http://www.csdn.net/article/2015-10-21/2825978)  
Android UI：机智的远程动态更新策略。随着需求的变化，某些入口界面会出现UI的增减、内容变化和跳转界面变化等问题。本文作者给出了一套方案来解决动态更新UI的问题以及更好地解决未读提醒的逻辑。

>20160119

* [给 App 提速：Android 性能优化总结](http://android.jobbole.com/81944/)  

本文是作者在Droidcon NYC会议上关于Android性能优化报告的一个总结，其中详细介绍了如何使用Systrace、Traceview、堆转储分配跟踪器、GPU 性能分析、层级观察器、硬件加速来进行App性能优化，介绍得比较系统全面，对实际的开发工作会有帮助。

>20160201

*[Android性能优化典范（四）](http://http://geek.csdn.net/news/detail/50692)，接上之前发的[性能优化1-3](http://www.kancloud.cn/kancloud/android-performance/53237)

>20160202

[Activity 与 Fragment 通信 较好解决方案](http://gold.xitu.io/entry/56a87b2b2e958a0051906227?utm_source=glowpost&utm_medium=20160130&utm_campaign=weibo)，- 能否有一种更好的方案来解决：Android 中 Activity 与 Fragment 之间通信的问题，什么叫更好呢，就是能让 Fragment 的复用性高，性能还有好（不用反射）

>20160504

[web缓存总结](http://www.alloyteam.com/2016/03/discussion-on-web-caching/)总结了传统web缓存相关的知识，各种头的作用和缓存的工作流程。

>20160505

[Android性能优化典范（五）](http://geek.csdn.net/news/detail/71031)，属于之前发的Android性能优化典范系列1-4的后续

##Gradle、打包发布相关

>20150831

* [如何使用Android Studio把自己的Android library分发到jCenter和Maven Central](http://inthecheesefactory.com/blog/how-to-upload-library-to-jcenter-maven-central-as-dependency/en)

本文讲解了通过下边的这行代码获得一个library的原理，同时详细讲解了如何使用Android Studio把自己的Android library分发到jCenter和Maven Central，需要使用的时候可以拿来作参考。

    dependencies {
        compile 'com.inthecheesefactory.thecheeselibrary:fb-like:0.9.3'
    }

>20160126

* [美团Android自动化之旅—生成渠道包](http://tech.meituan.com/mt-apk-packaging.html)

讲解了 3 种打包方式: 1. Maven, 2. apktool, 3. META-INF。其中第 3 种是一种比较快速的快速打包方式，通过生成母包，复制apk包并插入空文件的方式生成渠道包。避免了各个渠道依赖解析等过程。

另外推荐个第三方插件，[packer-ng-plugin](https://github.com/mcxiaoke/packer-ng-plugin)。严选这边已经开始用了，原来的打包近 `30` 个渠道包，顺利的话需要近 `1` 个小时；现在打近 `140` 个包，只需 `5` 分钟

>20160107

* [multidex对app启动速度的影响](https://medium.com/groupon-eng/android-s-multidex-slows-down-app-startup-d9f10b46770f#.otnf954xo)

之前郑大神也提到的，除非必要，请尽量不要开启multidex，本文分析了开启multidex可能会产生的问题，同时会影响app的启动速度，另外要开启multidex请严格按照Android Develop上的指导来做，当时二次元是没有设置MultiDexApplication的，导致mam接入的时候产生了bug。本文也提到了如何解决multidex影响app启动速度的问题。

>20160323

* [如何使用Android Studio开发Gradle插件](http://blog.csdn.net/sbsujjbcy/article/details/50782830),[Gradle for Android](https://segmentfault.com/a/1190000004229002 )

第一篇是介绍gradle插件开发的，第二篇是一系列翻译gradle for android的文章，但是好像并不完整。最近打算抽空做下MAM对1.5 android gradle plugin的支持，mark一下开始学习

>20160406

* [Android MultiDex实践：如何绕过那些坑？](http://mp.weixin.qq.com/s?__biz=MzA4MjU5NTY0NA==&mid=405574783&idx=1&sn=6ff49fda8a7229bf6b2692fddcf23e04&scene=0#wechat_redirect)

Android应用65k方法数的限制一直为广大开发者所诟病，Android官方给出的解决方案是MultiDex，但这里面其实有很多坑。作者对这些坑进行了分析，提出了解决方法，并且给出了一种改进的实现方法。

>20160511

* [从Instant-Run出发，谈谈Android上的热修复](http://zjutkz.net/2016/05/10/%E4%BB%8EInstant-Run%E5%87%BA%E5%8F%91%EF%BC%8C%E8%B0%88%E8%B0%88Android%E4%B8%8A%E7%9A%84%E7%83%AD%E4%BF%AE%E5%A4%8D/)

这篇文章从InstantRun出发，对Android中的几种热修复技术进行了分析。

## 进程、线程相关
>20160422

* [关于 Android 进程保活，你所需要知道的一切](http://www.jianshu.com/p/63aafe3c12af#)

文章对市面上常见的进程保活手段做了总结，包括在不同版本平台上使用系统漏洞来保活。除非被rom厂商加入白名单，否则不可能保证进程永生不死。


## framework

>20150906

* [MVP模式在Android开发中的应用](http://blog.csdn.net/vector_yi/article/details/24719873)

前几天看二次元的代码看到了很多Presenter，表示不解，所以学习了一下。这篇文章简单介绍了MVP模式的概念以及优缺点，同时给出了一个demo。另外，下面这篇文章给出了一个质疑的声音，称Activity严格来说不能等同于传统的View层，同时给出了作者觉得合适的命名。
[Don't call it MVP](http://www.philosophicalhacker.com/2015/04/05/dont-call-it-mvp/)

>20150917

* [ Android中的Apk的加固(加壳)原理解析和实现](http://blog.csdn.net/jiangwei0910410003/article/details/48415225)

之前调研反编译工具时，发现很多应用可以通过常用的反编译软件进行反编译，即便已经进行了混淆处理，可以从代码中发现一些重要的信息，
例如云阅读、二次元等android应用，可以简单被反编译。
本文主要对源Apk进行加密，然后在套上一层壳即可，介绍了主要原理和具体实现方法，包括加壳与脱壳处理。

>20150901

* [Android M 新的运行时权限开发者需要知道的一切](http://jijiaxin89.com/2015/08/30/Android-s-Runtime-Permission/)，android M新特性之一：权限运行时分配（这事自定义rom没少干）；对用户而言，动态分配意味可以对app更小粒度的权限分配，而不用为了使用app容忍其大量的流氓行为；对开发者而言，在使用api时必须考虑权限被拒绝的情况，身为一个懒惰的程序员，有没觉得一堆重复的运行时检查代码过于繁琐


这是邓际锋写的，关于FRP，很多人都知道这么个东西，但真正理解的人非常少。 [functional-reactive-programming](http://www.infoq.com/cn/articles/functional-reactive-programming)  FRP概念在移动端开发，非常有借鉴价值，做任务管理，数据依赖，使用FRP是一个全新的思路。

>20150925

[Android GUI系统](http://www.cnblogs.com/samchen2009/p/3364327.html)

>20150929

android 每日一读：[Android5.0中 Hwui 中 RenderThread 工作流程](http://androidperformance.com/2015/08/12/AndroidL-hwui-RenderThread-workflow/)
在 Android 4.x 时代，没有RenderThread，只有 Main Thread ，也就是说 必须要等到 Draw 完成后，才会去准备下一帧的数据。文章结合源码分析了Android 5.0 中 hwui 中的 RenderThread 的工作流程和原理。

>20151230

android每日一读[Android MVVM到底是啥？看完就明白了](http://mp.weixin.qq.com/s?__biz=MzA4MjU5NTY0NA==&mid=401410759&idx=1&sn=89f0e3ddf9f21f6a5d4de4388ef2c32f#rd)，文章从mvc开始，介绍了mvp和mvvm的模型，并重点介绍了mvvm的关键技术Data Binding Library。相关内容：[MVC，MVP 和 MVVM 的图示](http://www.ruanyifeng.com/blog/2015/02/mvcmvp_mvvm.html)

> 20160104

android每日一读:  [ Android中实现Activity的启动拦截之----实现360卫士的安装应用界面](http://blog.csdn.net/jiangwei0910410003/article/details/48787777#rd)  
作者介绍了一种使用进程注入方式拦截Activity的技术，可以实现应用锁、360的自定义安装界面等功能。

> 20160219

* [手淘Hotpatch技术介绍](http://www.infoq.com/cn/presentations/mobile-phone-taobao-hotpatch-technology-introduction
) 介绍了在手淘Hotpatch技术实现之前的App更新缺陷和为了更新而想到的一些方案，最后介绍手淘Dexposed技术在Hotpatch上的应用和基本原理（比较长，主要是演讲人说话比较慢=。=）

>20160224

* [浅析Android的窗口](http://bugly.qq.com/bbs/forum.php?mod=viewthread&tid=555&fromuid=6#rd)    
文章从android窗口的概念、分类以及窗口的创建和移除方面进行* 分析，并结合源码分析基本过程原理，让读者能从总体上对android框架中的各类窗口有个全面的认知。

>20160503

* [Android博客周刊专题之＃插件化开发＃](http://www.androidblog.cn/index.php/Index/detail/id/16)
非常好的一个插件化博客总结，从基础、入门、进阶和类库，由浅到深探讨了差价化的方方面面，感兴趣的同学可以花些时间看看，内容很多，但总结的确实很好

##语言相关
* [Kotlin介绍](https://docs.google.com/document/d/1ReS3ep-hjxWA8kZi0YqDbEhCqTt29hG8P44aA9W0DM8/edit?hl=en&forcehl=1#heading=h.ufyo552ni0as)    
本篇文档介绍了一个可以用于Android开发的语言——Kotlin。Kotlin是JetBrains公司开发的，被称为Android版的swift。相比Java，Kotlin更加安全和简洁，如果厌倦了使用Java开发Android，或许可以试试Kotlin。

>20160314

* [从Java代码到机器代码：如何编写高度优化的Java程序](http://www.infoq.com/cn/presentations/from-java-code-to-machine-code?utm_campaign=rightbar_v2&utm_source=infoq&utm_medium=presentations_link&utm_content=link_text)    
这个演讲视频了介绍编译和优化过程，并将通过实际案例来说明：在编写Java代码时，遵循一些简单的规则，即可获得高度优化的、高性能的程序。

>20160518

* [详细分析Java中断机制](http://www.infoq.com/cn/articles/java-interrupt-mechanism)
讲述了 Java 中断机制的原理，使用场景和捕获中断后处理情况等

##设计模式相关

>20150918

* [Android系统中的设计模式](https://github.com/simple-android-framework-exchange/android_design_patterns_analysis)
这是一个开源项目，结合android源码，分析了Android系统中的设计模式，不足的地方是，代码都是在文章中贴出来的，没有可以运行的demo，并且这个项目现在已经停止更新了

>20151012

* [面相对象六大设计原则](https://github.com/simple-android-framework-exchange/android_design_patterns_analysis/blob/master/oop-principles/oop-principles.md)
本文结合volley源码介绍了面向对象的六大设计原则，单一职责、里氏替换、依赖倒置、开闭原则、接口隔离原则、迪米特原则，如果觉得自己的代码接口设计混乱、代码耦合较为严重、一个类的代码过多等等，不妨学习、熟悉下这些原则，尝试写出整洁的代码、清晰简单的接口、职责单一的类。

>20151202

* [如何在Android开发中使用RxJava 提升用户体验一](http://www.jianshu.com/p/33c548bce571)
* [如何在Android开发中使用RxJava 提升用户体验二](http://blog.csdn.net/lzyzsd/article/details/50120801#0-tsina-1-39222-397232819ff9a47a7b7e80a40613cfe1)
如何在Android开发中使用RxJava 提升用户体验

>20160217

[A detailed guide on developing Android apps using the Clean Architecture pattern
](https://medium.com/@dmilicic/a-detailed-guide-on-developing-android-apps-using-the-clean-architecture-pattern-d38d71e94029#.bi8cnk7on)

Clean Architecture是洋葱架构的一种变形，设计的思想是是单向依赖关系，外部的层能够访问内部的层，而内部的层则对外部的层一无所知。本文介绍了干净架构在android上的应用，提供了两个比较完整的实例

>20160229

* [如何设计MVP中的Presentation层](http://blog.chengdazhi.com/index.php/115)

有很多项目设计MVP架构时，分不清哪些代码属于Presenter而哪些代码属于View(UI)，这就是写这篇文章的目的。

##新闻资讯类

>20151030

* [Android5.0录屏漏洞及其简单应用](http://drops.wooyun.org/papers/9769)
之前爆过的一个Android5.0的漏洞，可以被不法分子利用进行录屏操作的，警示开发者和使用者注意安全。目前Google已发布补丁。安全这种事真是刻不容缓呀！

>20151231

* [论客户端埋点](https://testerhome.com/topics/3762)
用户数据的收集一直是持之以恒的话题,移动端的收集数据则是通过埋点来实现，埋点是艺术活，埋的好，可以给你带来漂亮的报表，有钱途的业务模型等等。埋的不好，数据没有用，还占资源。

##开发工具
>20151105

* [倍数提高工作效率的Android Studio奇技](http://zlv.me/posts/2015/07/13/14_android-studio-tips/)
这是从Philippe Breault的系列文章《Android Studio Tips Of the Day》中提取出来的自认为精华的部分。 这些技巧在实际应用中能够非常大的提高工作效率。

附上原文：[android-studio-tips-of-the-day](http://www.developerphil.com/android-studio-tips-of-the-day-roundup-1/)

>20151225

* [开发者选项都是干什么用的](http://www.jianshu.com/p/07b551ee260b) 极简单的总结，两分钟就能看完。开发的时候可以辅助着用一下，可能会有新发现哟。

>20160112

* [Qt on Android](http://www.kdab.com/qt-on-android-episode-1/#more-4283
)这篇文章简要的介绍了Qt及Qt on Android的由来，同时博客里面也有教学怎么写的，不过很简单。关于其优势和劣势的讨论可以见[知乎](http://www.zhihu.com/question/19689965
), 同时我试着自己搭了一下环境并写了一下demo发现并不太好写。另外有[国人编写和翻译的博客以及书籍](http://blog.csdn.net/column/details/qt-on-android.html?&page=2
)


##算法
>20151229

* [Bloom Filter概念和原理](http://blog.csdn.net/jiaomeng/article/details/1495500) 在计算机科学中，我们常常会碰到时间换空间或者空间换时间的情况，即为了达到某一个方面的最优而牺牲另一个方面。Bloom Filter在时间空间这两个因素之外又引入了另一个因素：错误率。在使用Bloom Filter判断一个元素是否属于某个集合时，会有一定的错误率。也就是说，有可能把不属于这个集合的元素误认为属于这个集合（False Positive），但不会把属于这个集合的元素误认为不属于这个集合（False Negative）。在增加了错误率这个因素之后，Bloom Filter通过允许少量的错误来节省大量的存储空间。

##API设计相关
>20160115

* [Google首席软件工程师Joshua Bloch谈如何设计一款优秀的API ](http://www.csdn.net/article/2014-02-18/2818441-How-to-design-a-good-API#rd )

随着大数据、公共平台等互联网技术的日益成熟，API接口的重要性日益凸显，文章中首先对优秀API的特点进行说明，并介绍api设计的注意事项和原则，随后罗列了api中的类、方法和异常处理等的设计规则。

>20160225

* [开发一流的 Android SDK： Fabric SDK 的创建经验](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2016/0216/3967.html)

Fabric团队展示了创建 Fabric SDK 过程中，学到的各种经验心得，关于稳定性、性能、SDK 体积控制、以及对于一些特殊情况的处理这些方面，相信对大家能收益很多关于设计 SDK 的伟大想法。

# Android安全
>20160412

* [APK瘦身记，如何实现高达53%的压缩效果](https://mp.weixin.qq.com/s?__biz=MzIwMTI4Nzk5Ng==&mid=402517579&idx=1&sn=2951ec2b3aef4ce6f6a5c06ad4c49d73) 

从Apk瘦身的几个切入点出发，对于apk瘦身的一些尝试和瘦身的一个效果

>20160415

* [android java hook 那点事(1)](http://www.9hao.info/pages/2014/03/android-java-hook-na-dian-shi-1) 和 [android java hook 那点事(2)](http://www.9hao.info/pages/2014/05/android-java-hook-na-dian-shi-2)。最近在看 Dexposed 时，查到的一点资料，讲述了当 Dalvik 虚拟机加载java函数的时候，是如何选择执行其对应的字节码还是执行 native 方法，如何修改一个 java 方法为 native 方法比较等。较为清楚的讲述了 Dexposed 核心原理。

##源码阅读
>20160302

* [阅读Android源码的一些姿势](http://zhuanlan.zhihu.com/kaede/20564614)
1）推荐了Google的Android开源项目(AOSP)。2）推荐了几个辅助源码阅读的工具。3）最重要的是分享了由浅及深阅读源码的顺序。

##技术无关
>20160201

* [2015年，移动开发都有哪些热点](http://www.infoq.com/cn/articles/mobile-trend-2015)
1) 讲述了当前移动开发的热点，如 Famo.us，J2OBJC，Xamarin，React Native.

*[怎么做好互联网公司的技术团队负责人](https://zybuluo.com/liter/note/266163) ，笔者从业务、团队、技术三个层面讨论，分享了自己作为客户端负责人的一些经验之谈。。感觉挺不错的。。@各位技术大神。。。


>20160418

* [涅槃重生:我的技术转管理之路](http://mp.weixin.qq.com/s?__biz=MjM5NTIyNTUyMQ==&mid=437927167&idx=1&sn=9e5cc72546c1111b335bbbb71b8318bc&scene=0&key=ac89cba618d2d97635ebfdea222c6d87a6da37221e1c8ad8703d028d79f964f533877ceb05baba85aab84a363c4e25c8&ascene=0&uin=MTYzMjY2MTE1&devicetype=iMac+MacBookPro10%2C1+OSX+OSX+10.11.2+build(15C50)&version=11020201&pass_ticket=8%2B9kCPaKWLELWhXK1Ti56wnYFeHN%2Flwihti1k%2FcCTMw%3D) ,虽然不知道何年何月，会不会走上这条道路，但是补充点知识总是好的。