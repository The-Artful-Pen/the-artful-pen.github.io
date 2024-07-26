# 前言
大家在浏览独立博客网站时可能会发现，有的网站内有个类似于手机WI-FI标志的按钮，这其实是RSS（简易信息聚合）订阅。以[本站](https://[peter267.github.io//rss.xml](https://peter267.github.io//rss.xml))为例，它左上角有个RSS订阅功能，当我们点击后，会得到一个格式为xml格式的文件。那么，RSS是什么，为什么，怎么用呢
# 是什么
>引用自[百度百科](https://baike.baidu.com/item/RSS/24470)
[简易信息聚合](https://baike.baidu.com/item/%E7%AE%80%E6%98%93%E4%BF%A1%E6%81%AF%E8%81%9A%E5%90%88/6453727?fromModule=lemma_inlink)（也叫聚合内容）是一种基于XML的标准，在互联网上被广泛采用的内容包装和投递协议。RSS(Really Simple Syndication)是一种描述和同步网站内容的格式，是使用最广泛的XML应用。RSS搭建了信息迅速传播的一个技术平台，使得每个人都成为潜在的[信息提供者](https://baike.baidu.com/item/%E4%BF%A1%E6%81%AF%E6%8F%90%E4%BE%9B%E8%80%85/12754057?fromModule=lemma_inlink)。发布一个RSS文件后，这个RSS [Feed](https://baike.baidu.com/item/Feed/15181?fromModule=lemma_inlink)中包含的信息就能直接被其他站点调用，而且由于这些数据都是标准的XML格式，所以也能在其他的终端和服务中使用，是一种描述和同步[网站内容](https://baike.baidu.com/item/%E7%BD%91%E7%AB%99%E5%86%85%E5%AE%B9/6694752?fromModule=lemma_inlink)的格式。 [1]RSS可以是以下三个解释的其中一个： Really Simple Syndication；RDF (Resource Description Framework) Site Summary； Rich Site Summary。但其实这三个解释都是指同一种Syndication的技术。
RSS广泛用于网上新闻频道，[blog](https://baike.baidu.com/item/blog/8086465?fromModule=lemma_inlink)和[wiki](https://baike.baidu.com/item/wiki/97755?fromModule=lemma_inlink)，主要的版本有0.91, 1.0, 2.0。使用[RSS订阅](https://baike.baidu.com/item/RSS%E8%AE%A2%E9%98%85/663114?fromModule=lemma_inlink)**能更快地获取信息**，网站提供RSS输出，有**利于让用户获取网站内容的最新更新**。[网络用户](https://baike.baidu.com/item/%E7%BD%91%E7%BB%9C%E7%94%A8%E6%88%B7/56340765?fromModule=lemma_inlink)可以在客户端借助于支持RSS的聚合工具软件，**在不打开网站内容页面的情况下阅读支持RSS输出的网站内容**。

说了这么多，你可以简单的把它理解为**把多个平台的内容汇聚在一起，让你能在一个平台上看到**
# 为什么
如果你关注了多个博主（信号源），每天都要看一遍他们有没有更新，要奔波于各个网站，应用之间。RSS把这些内容汇聚到了一起，让你在一个平台上观看，还能避免博客平台的“垃圾信息和广告”，让你有个安静的阅读环境，我想这就是RSS的意义
# 怎么用
## 对于有RSS功能的网页
建议使用[QiReader](https://www.qireader.com.cn/)，这是一个界面现代的RSS阅读器，进入官网后点击注册，注册账号后点击添加内容，在输入框内输入-点击RSS按钮后出现的网页的网址链接-，直接复制过去回车，点击订阅即可
![屏幕截图 2024-07-25 154933](https://github.com/user-attachments/assets/be41f273-7bb6-4fb7-89f8-9047d977142d)
## 对于无RSS功能的网页
建议使用[RSSHub](https://docs.rsshub.app/zh/)和[Fluent-Reader](https://github.com/yang991178/fluent-reader)
1. 进入[Fluent-Reader](https://github.com/yang991178/fluent-reader)后，记得先star支持下作者。点击Releases下的第一个按钮，选择适合自己电脑的版本，点击下载。
2. 进入[RSSHub](https://docs.rsshub.app/zh/guide/)，点击“食用指南”，在左侧找到想订阅的博客类型，在右侧寻找博客，再在博客的细分类中找到自己要订阅的源，点击。
3. 我以-论坛-百度-精品帖子-为例，点击后复制Example后的链接，链接后有一个复制按钮，点击以复制。
4. 打开Fluent-Reader，在右上角设置-添加订阅源-栏里粘贴复制的链接，**不要点击“添加”**
5. **重要的一步**，在RSSHub中打开“公共实例”，在Public表中找到一个可用“Online列为up”的URL，选中复制
6. 回到Fluent-Reader，把填进去的链接中“rsshub.app”替换成你复制的链接，点击添加，大功告成！
![屏幕截图 2024-07-26 134635](https://github.com/user-attachments/assets/4743e26f-4829-47de-bd0a-7a57146dd8ab)
> [!NOTE]
> [视频版教程](https://www.bilibili.com/video/BV1mz42197g1/)

> [!TIP]
> 但凡在Github下载过东西的都知道它下载的有多慢，我把Fluent-Reader的下载程序放到网盘里了，需要自取[123网盘](https://www.123pan.com/s/hoPKVv-2aB63.html)

> [!NOTE]
> 其实使用[RSSHub](https://docs.rsshub.app/zh/)和[QiReader](https://www.qireader.com.cn/)搭配也可以，甚至不用更换“rsshub.app"了（应该），对于有RSS功能的网页，也可以使用Fluent-Reader。但是QiReader功能较少，但方便。可以选择自己喜欢的。