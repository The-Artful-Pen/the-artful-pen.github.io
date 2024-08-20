> 温馨提示，本文章转载自[Meekdai-Gmeek快速上手](https://blog.meekdai.com/post/Gmeek-kuai-su-shang-shou.html)，但我认为本文比原文更加细致

[Gmeek](https://github.com/Meekdai/Gmeek) 是一个博客框架，超轻量级个人博客模板，完全基于`Github Pages` 、 `Github Issues` 和 `Github Actions`，可以称作`All in Github`。不需要本地部署，从搭建到写作，只需要18秒，2步搭建好博客，第3步就是写作。
## 一、安装

> 安装及其简单，但是也要认真看下面的步骤，一步一步来。

【创建仓库】点击[通过模板创建仓库](https://github.com/new?template_name=Gmeek-template&template_owner=Meekdai)，建议仓库名称为`XXX.github.io`，其中`XXX`为你的github用户名。（例如我的名字是Peter267，则我的仓库名称应为peter267.github.io，全部小写）

【启用Pages】在仓库的设置`Setting`s中`Pages->Build and deployment->Source`下面选择`Github Actions`。
  
[![pAPIwgU.png](https://s21.ax1x.com/2024/08/20/pAPIwgU.png)](https://imgse.com/i/pAPIwgU)

【开始写作】打开一篇issue，开始写作，并且必须添加一个标签Label（至少添加一个），再保存issue（点击Submit new issue）后会自动创建博客内容，片刻后可通过https://xxx.github.io/ 访问（可进入Actions页面查看构建进度）。

 [![pAPI6ER.png](https://s21.ax1x.com/2024/08/20/pAPI6ER.png)](https://imgse.com/i/pAPI6ER)

 [![pAPIRC6.png](https://s21.ax1x.com/2024/08/20/pAPIRC6.png)](https://imgse.com/i/pAPIRC6)
[![pAPokGV.png](https://s21.ax1x.com/2024/08/20/pAPokGV.png)](https://imgse.com/i/pAPokGV)

【手动全局生成】这个步骤只有在修改config.json 文件或者出现奇怪问题的时候，需要执行。
 
[![pAPouZ9.png](https://s21.ax1x.com/2024/08/20/pAPouZ9.png)](https://imgse.com/i/pAPouZ9)

## 二、配置文件

> 按照安装步骤成功搭建好后，就可以阅读下面的内容修改配置文件啦。
注意修改配置文件后一定要手动全局生成一次，不然会报错。
如果对`json`格式不熟悉，建议先简单学习一下。

`config.json` 文件就是配置文件，在创建的仓库内可以找到，对应修改为自己的即可。
```
{
    "title":"Meekdai",
    "subTitle":"童话是一种生活态度，仅此而已。",
    "avatarUrl":"https://github.githubassets.com/favicons/favicon.svg",
    "GMEEK_VERSION":"last"
}
```
以上是必须的字段，下面是可以自定义字段的描述，可以选择加入到`config.json`中。
```
"displayTitle":"Meekdai",
"homeUrl":"http://blog.meekdai.com",
"faviconUrl":"https://github.githubassets.com/favicons/favicon.svg",
"email":"meekdai@163.com",
"startSite":"02/16/2015",
"filingNum":"浙ICP备20023628号",
"onePageListNum":15,
"singlePage":["about"],
"iconList":{"music":"M0 8a8 8 0 1 1 16 0A8 8 0 0 1 0 8Zm8-6.5a6.5 6.5 0 1 0 0 13 6.5 6.5 0 0 0 0-13Z"},
"exlink":{"music":"https://music.meekdai.com"},
"commentLabelColor":"#006b75",
"yearColorList":["#bc4c00", "#0969da", "#1f883d", "#A333D0"],
"i18n":"CN",
"UTC":8,
"themeMode":"manual",
"dayTheme":"light",
"nightTheme":"dark_colorblind",
"urlMode":"pinyin",
"style":"",
"script":"",
"head":"",
"allHead":"",
"indexStyle":"",
"indexScript":"",
"showPostSource":1,
"rssSplit":"sentence",
"bottomText":"转载请注明出处",
"ogImage":"https://cdn.jsdelivr.net/gh/Meekdai/meekdai.github.io/logo64.jpg",
"primerCSS":"<link href='https://mirrors.sustech.edu.cn/cdnjs/ajax/libs/Primer/21.0.7/primer.css' rel='stylesheet' />",
"needComment":0,
```
 [![pAPoTQU.png](https://s21.ax1x.com/2024/08/20/pAPoTQU.png)](https://imgse.com/i/pAPoTQU)
| 配置参数      | 说明 |
| ----------- | ----------- |
| title| 【必填】博客标题       |
| subTitle   | 【必填】博客描述&自述        |
 |   avatarUrl     |   【必填】博客头像        |
 |  GMEEK_VERSION        |    【必填】Gmeek版本，一般写last也可以用具体tag版本     |
 | displayTitle         | 用于头像后面的标题展示，如果和`title`一致则不用添加       |
 | homeUrl         |  博客的主页地址，自定义域名时需要配置        |
 |   faviconUrl       | 页面的favicon地址，如果和`avatarUrl`一致则不用添加         |
 |  email        |    用于自动提交仓库时用，不添加也可以      |
 |  startSite        |  用于页面底部显示网站运行天数        |
 |   filingNum       |   用于页面底部显示备案信息（未备案请不要添加）       |
 |  onePageListNum        |  用于首页每页展示的文章数量        |
 |   singlePage       | 自定义独立页面，例如`about`或者`link`等         |
 |  iconList        |  用于定义singlePage按钮展示的[SVG图标](https://primer.style/foundations/icons/#16px) (16px)，`about`和`link`内置无需定义        |
 | exlink         |  用于自定义首页右上角圆形按钮到外部链接功能，按钮图标定义在iconList中        |
 |  commentLabelColor       |   用于自定义显示评论数量标签的颜色       |
 |   yearColorList       | 用于自定义显示不同年份标签的颜色       |
 |  i18n        |  用于定义博客语言，目前支持`EN`/`CN`/`RU`   （英文/中文/俄文）    |
 |  themeMode        | 用于定义主题模式，默认为`manual`，也可选择`fix`[详细说明](https://blog.meekdai.com/post/%E3%80%90Gmeek-jin-jie-%E3%80%91-liang-an-zhu-ti-pei-zhi-fang-shi.html)         |
 |  dayTheme        |  用于定义[亮主题](https://github.com/settings/appearance)        |
 |   nightTheme       |     用于定义[暗主题](https://github.com/settings/appearance)     |
 |   urlMode       |  用于定义文章链接生成模式，目前支持`pinyin`/`issue`/`ru_translit`  （文章标题拼音/issue序号（例：post7））/俄文      |
 |  style        |  用于自定义文章页CSS        |
 |   script       |  用于自定义文章页JavaScript        |
 |  head       |   用于自定义文章页head内容      |
 |  allHead        |    用于自定义所有页面head内容     |
 |    indexStyle      |  用于自定义首页CSS        |
 |  indexScript        |   用于自定义首页JavaScript       |
 |    showPostSource      |  设置为1则在文章页显示issue链接按钮，设置为0则不显示        |
 |   rssSplit       | 设置RSS输出的截断符号，默认`sentence`为第一句话，可配置其他特殊符号        |
 | bottomText         |    用于设置文章页面右下角显示的内容      |
 | ogImage         | 用于设置Open Graph协议展示的图片         |
 |  primerCSS        | 用于设置primer.css的CDN地址，默认使用[南科大](https://mirrors.sustech.edu.cn/cdnjs/ajax/libs/Primer/21.0.7/primer.css)         |
 |    needComment      | [用于设置是否需要评论功能，1开启评论，0关闭（如果想使用评论，请[下载utterances评论](https://github.com/apps/utterances)）      |
## 三、代码示范
### ✅ 正确代码
```
{
    "title":"Peter's Blog",
    "subTitle":"无限进步！",
    "avatarUrl":"https://i1.hdslb.com/bfs/face/4963f665e12a4703a1c54adc252fcae4b7e93005.jpg",
    "faviconUrl":"https://vip.helloimg.com/i/2024/07/31/66aa2568dfba1.png",
    "displayTitle":"Peter Tech",
    "singlePage":["link","about","thinkbox"],
    "iconList":{"thinkbox":"m8.878.392 5.25 3.045c.54.314.872.89.872 1.514v6.098a1.75 1.75 0 0 1-.872 1.514l-5.25 3.045a1.75 1.75 0 0 1-1.756 0l-5.25-3.045A1.75 1.75 0 0 1 1 11.049V4.951c0-.624.332-1.201.872-1.514L7.122.392a1.75 1.75 0 0 1 1.756 0ZM7.875 1.69l-4.63 2.685L8 7.133l4.755-2.758-4.63-2.685a.248.248 0 0 0-.25 0ZM2.5 5.677v5.372c0 .09.047.171.125.216l4.625 2.683V8.432Zm6.25 8.271 4.625-2.683a.25.25 0 0 0 .125-.216V5.677L8.75 8.432Z"},
    "homeUrl":"https://peter267.github.io/",
    "email":"miaomiaoweiqi@163.com",
    "startSite":"07/18/2024",
    "onePageListNum":15,
    "commentLabelColor":"#006b75",
    "yearColorList":["#bc4c00", "#0969da", "#1f883d", "#A333D0"],
    "i18n":"CN",
    "UTC":8,
    "themeMode":"manual",
    "dayTheme":"light",
    "nightTheme":"dark_colorblind",
    "urlMode":"issue",
    "rssSplit":"sentence",
    "bottomText":"❤️ 转载文章请注明出处，谢谢！❤️",
    "ogImage":"https://i1.hdslb.com/bfs/face/4963f665e12a4703a1c54adc252fcae4b7e93005.jpg@240w_240h_1c_1s_!web-avatar-nav.avif",
    "primerCSS":"<link href='https://mirrors.sustech.edu.cn/cdnjs/ajax/libs/Primer/21.0.7/primer.css' rel='stylesheet' />",
    "needComment":1,
    "script":"<script>document.getElementById('cmButton').click();</script>",
    "allHead":"<script src='https://blog.meekdai.com/assets/GmeekVercount.js'></script>",
    "script":"<script src='https://blog.meekdai.com/Gmeek/plugins/GmeekTOC.js'></script><script src='https://blog.meekdai.com/Gmeek/plugins/lightbox.js'></script>",
    "GMEEK_VERSION":"last"
}
```

- 代码开头结尾应该有 “{” 和 “}” 符号
- 每行代码后方有个英文逗号（,），最后一行代码除外
- 每行代码开头空四格（ “{”和 “}”除外）
### ❌ 错误代码
```
{
    "title":"Peter's Blog",
    "subTitle":"无限进步！",
    "avatarUrl":"https://i1.hdslb.com/bfs/face/4963f665e12a4703a1c54adc252fcae4b7e93005.jpg",
    "faviconUrl":"https://vip.helloimg.com/i/2024/07/31/66aa2568dfba1.png",
}
    "displayTitle":"Peter Tech",
    "singlePage":["link","about","thinkbox"],
    "iconList":{"thinkbox":"m8.878.392 5.25 3.045c.54.314.872.89.872 1.514v6.098a1.75 1.75 0 0 1-.872 1.514l-5.25 3.045a1.75 1.75 0 0 1-1.756 0l-5.25-3.045A1.75 1.75 0 0 1 1 11.049V4.951c0-.624.332-1.201.872-1.514L7.122.392a1.75 1.75 0 0 1 1.756 0ZM7.875 1.69l-4.63 2.685L8 7.133l4.755-2.758-4.63-2.685a.248.248 0 0 0-.25 0ZM2.5 5.677v5.372c0 .09.047.171.125.216l4.625 2.683V8.432Zm6.25 8.271 4.625-2.683a.25.25 0 0 0 .125-.216V5.677L8.75 8.432Z"},
    "homeUrl":"https://peter267.github.io/",
    "email":"miaomiaoweiqi@163.com",
    "startSite":"07/18/2024",
    "onePageListNum":15,
    "commentLabelColor":"#006b75",
    "yearColorList":["#bc4c00", "#0969da", "#1f883d", "#A333D0"],
    "i18n":"CN",
    "UTC":8,
    "themeMode":"manual",
    "dayTheme":"light",
    "nightTheme":"dark_colorblind",
    "urlMode":"issue",
    "rssSplit":"sentence",
    "bottomText":"❤️ 转载文章请注明出处，谢谢！❤️",
    "ogImage":"https://i1.hdslb.com/bfs/face/4963f665e12a4703a1c54adc252fcae4b7e93005.jpg@240w_240h_1c_1s_!web-avatar-nav.avif",
    "primerCSS":"<link href='https://mirrors.sustech.edu.cn/cdnjs/ajax/libs/Primer/21.0.7/primer.css' rel='stylesheet' />",
    "needComment":1,
    "script":"<script>document.getElementById('cmButton').click();</script>",
    "allHead":"<script src='https://blog.meekdai.com/assets/GmeekVercount.js'></script>",
    "script":"<script src='https://blog.meekdai.com/Gmeek/plugins/GmeekTOC.js'></script><script src='https://blog.meekdai.com/Gmeek/plugins/lightbox.js'></script>",
    "GMEEK_VERSION":"last"
```
问题原因：格式错误
```
{
    "title":"Peter's Blog",
    "subTitle":"无限进步！",
    "avatarUrl":"https://i1.hdslb.com/bfs/face/4963f665e12a4703a1c54adc252fcae4b7e93005.jpg",
    "faviconUrl":"https://vip.helloimg.com/i/2024/07/31/66aa2568dfba1.png",
}
    "displayTitle":"Peter Tech",
    "singlePage":["link","about","thinkbox"],
    "iconList":{"thinkbox":"m8.878.392 5.25 3.045c.54.314.872.89.872 1.514v6.098a1.75 1.75 0 0 1-.872 1.514l-5.25 3.045a1.75 1.75 0 0 1-1.756 0l-5.25-3.045A1.75 1.75 0 0 1 1 11.049V4.951c0-.624.332-1.201.872-1.514L7.122.392a1.75 1.75 0 0 1 1.756 0ZM7.875 1.69l-4.63 2.685L8 7.133l4.755-2.758-4.63-2.685a.248.248 0 0 0-.25 0ZM2.5 5.677v5.372c0 .09.047.171.125.216l4.625 2.683V8.432Zm6.25 8.271 4.625-2.683a.25.25 0 0 0 .125-.216V5.677L8.75 8.432Z"},
    "homeUrl":"https://peter267.github.io/",
    "email":"miaomiaoweiqi@163.com",
    "startSite":"07/18/2024",
    "onePageListNum":15,
"commentLabelColor":"#006b75",
"yearColorList":["#bc4c00", "#0969da", "#1f883d", "#A333D0"],
"i18n":"CN",
"UTC":8,
"themeMode":"manual",
"dayTheme":"light",
"nightTheme":"dark_colorblind",
"urlMode":"issue",
"rssSplit":"sentence",
"bottomText":"❤️ 转载文章请注明出处，谢谢！❤️",
"ogImage":"https://i1.hdslb.com/bfs/face/4963f665e12a4703a1c54adc252fcae4b7e93005.jpg@240w_240h_1c_1s_!web-avatar-nav.avif",
"primerCSS":"<link href='https://mirrors.sustech.edu.cn/cdnjs/ajax/libs/Primer/21.0.7/primer.css' rel='stylesheet' />",
"needComment":1,
"script":"<script>document.getElementById('cmButton').click();</script>",
"allHead":"<script src='https://blog.meekdai.com/assets/GmeekVercount.js'></script>",
"script":"<script src='https://blog.meekdai.com/Gmeek/plugins/GmeekTOC.js'></script><script src='https://blog.meekdai.com/Gmeek/plugins/lightbox.js'></script>",
"GMEEK_VERSION":"last"
```
问题原因：缩进错误
## 四、常见问题
### 1. 搭建不成功
多半是没有按照安装步骤来，其实搭建就这2步，不要自己乱点乱设置，就不会有问题。

- 案例一：https://github.com/Meekdai/Gmeek/issues/14
- 案例二：https://github.com/Meekdai/Gmeek/issues/18
- 案例三：https://github.com/Meekdai/Gmeek/issues/20
### 2. Actions执行失败
修改了`config.json`配置文件后，需要全局生成。另外label标签没有打会出现这个问题。
建议通过Actions->build Gmeek->Run workflow->里面的按钮全局重新生成一次

- 案例一：https://github.com/Meekdai/Gmeek/issues/1
- 案例二：https://github.com/Meekdai/Gmeek/issues/10
### 3. 导入以前的文章
如需修改发布时间，可以在文章最后一行添加如下代码。里面的时间是采用时间戳的形式，可以用如下[网站](https://tool.lu/timestamp)转换。
```
<!-- ##{"timestamp":1490764800}## -->
```
### 4. 自定义单篇文章参数
自定义单篇文章页面的`style`和`script`

```
<!-- ##{"style":"<style>#postBody{font-size:20px}</style>"}## -->
```

<!-- ##{"script":"<script async src='//busuanzi.ibruce.info/busuanzi/2.3/busuanzi.pure.mini.js'></script>"}## -->
### 5. 多种自定义参数
可同时一起添加多种自定义参数：

```
<!-- ##{"script":"<script async src='//busuanzi.ibruce.info/busuanzi/2.3/busuanzi.pure.mini.js'></script>","style":"<style>#postBody{font-size:20px}</style>","timestamp":1490764800}## -->
```

### 6. 自定义全局文章参数
添加全局文章页面的`style`和`script`，在`config.json`文件中添加

```
"style":"<style>#postBody{font-size:20px}</style>",
"script":"<script async src='//busuanzi.ibruce.info/busuanzi/2.3/busuanzi.pure.mini.js'></script>",
```

### 7. 置顶博客文章
只需要`Pin issue`后，手动全局生成一次即可。
### 8. utteranc报错
如果在评论里面登录后评论报错，可直接按照提示安装utteranc app即可

```
Error: utterances is not installed on xxx/xxx.github.io. If you own this repo, install the app. Read more about this change in the PR.
```

### 9. 删除文章
只需要Close issue或者Delete issue后，再手动全局生成一次即可。
