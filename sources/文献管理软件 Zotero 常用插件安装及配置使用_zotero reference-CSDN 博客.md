> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [blog.csdn.net](https://blog.csdn.net/qq_43309940/article/details/117126357)

#### 文献管理软件 - Zotero 常用插件安装及配置使用

*   [一、Zotero 安装与同步盘配置](#Zotero_2)
*   *   [1、下载 Zotero 并安装](#1Zotero_3)
    *   [2、配置 Zotero](#2Zotero_18)
    *   *   [（1）配置同步盘（以 onedrive 为例）——如果不配置同步盘，这一步可以跳过](#1onedrive_19)
        *   [（2）配置输出文献引用格式](#2_39)
        *   [（3）Zotero+ Sci-Hub](#3Zotero_SciHub_55)
*   [二、安装 Zotero 常用插件](#Zotero_88)
*   *   [1、ZotFile 插件（最重要的插件）](#1ZotFile__93)
    *   *   [（1）ZotFile 插件下载](#1ZotFile__100)
        *   [（2）ZotFile 插件安装](#2ZotFile__108)
        *   [（3）重启 Zotero](#3Zotero_110)
        *   [（4）ZotFile 插件配置](#4ZotFile_113)
    *   [2、Zotero translators 插件](#2Zotero_translators_123)
    *   *   [（1）Zotero translators 介绍及下载](#1Zotero_translators_124)
        *   [（2）Zotero translators 安装](#2Zotero_translators_135)
        *   [（3）Zotero translators 插件更新](#3Zotero_translators_143)
    *   [3、 Jasminum 插件](#3_Jasminum_147)
    *   *   [（1）功能介绍及下载](#1_148)
        *   [（2）安装 Jasminum 插件](#2Jasminum_160)
        *   [（3）安装 PDFtk server](#3PDFtk_server_163)
        *   [（4）配置 Jasminum 插件](#4Jasminum_169)
        *   [（5）Jasminum 使用](#5Jasminum_173)
    *   [4、Zotero IF 插件（Zotero IF v1.10）](#4Zotero_IF_Zotero_IF_v110_184)
    *   [5、 delitemwithatt 插件](#5_delitemwithatt__201)
    *   [6、zotero-pdf-translate 插件（内置阅读器划线翻译插件）](#6zoteropdftranslate__216)
    *   [7、zotero-doi-manager 插件（自动获取 doi）](#7zoterodoimanagerdoi_226)
    *   [8、zotero-reference 插件（自动获取参考文献）](#8zoteroreference_243)

一、Zotero 安装与同步盘配置
-----------------

### 1、下载 Zotero 并安装

（[点此链接进入下载](https://www.zotero.org/download/)）

![](https://i-blog.csdnimg.cn/blog_migrate/031b183efdfe215850ad079d5f1f5296.png)  
注意：此部分需要安装两个东西，一个是安装 Zotero 主程序另一个是安装 Zotero connector 插件，使用不同浏览器下载时会自动显示和该浏览器匹配的 Zotero connector 插件（上述图片是使用 edge 打开显示的下载界面），安装完成后在浏览器插件栏会出现如下图标：  
![](https://i-blog.csdnimg.cn/blog_migrate/c7a110965bca5af8a9aa7ef54b0a55de.png)  
chrome 浏览器的插件如果无法下载的可以从下面下载（打开 chrome 浏览器 “扩展程序” 界面后打开“开发者选项”，再将 zip 文件直接拖入扩展程序界面即可完成安装）

> https://wwd.lanzouj.com/iyox107f4xlg  
> 密码: hgoi

使用方法：  
在文献下载页面点击该插件可直接对文献进行下载，多篇文献出现时该插件图标变为下图文件夹形式，可选择自己需要的文献下载，单篇文献时直接下载，具体可自行体验。  
![](https://i-blog.csdnimg.cn/blog_migrate/ee7def3eea5d3b6eeafe8790d0e46995.png)

### 2、配置 Zotero

#### （1）配置同步盘（以 onedrive 为例）——如果不配置同步盘，这一步可以跳过

由于 Zotero 提供的云盘只有 300M 的空间，因此需要配合其他的云盘进行同步，本文使用 Onedrive 作为同步盘（认证学生可以获取 1T 的免费空间）

①点击编辑 -> 首选项，弹出 zotero 首选项设置窗口  
![](https://i-blog.csdnimg.cn/blog_migrate/76374997c05c4041e2d83b7995853290.png)  
②点击同步 -> 设置：文件同步的两个选项都取消  
![](https://i-blog.csdnimg.cn/blog_migrate/730da30188579209f7b9c8164110a27b.png)  
③点击高级 -> 文件和文件夹：这部分需要设置两个路径，一个是数据存储位置，可以选择默认也可以自己设置，这部分保存的是文献信息占用空间较小，因此这里选择默认；第二个是根目录的设置，这里的更目录选择的是 Zotero 文件夹的绝对位置，这里设置好以后之后的其他文件都会以该路径作为相对路径，而将这个绝对路径设置在 OneDrive 同步盘路径下就可以通过 OneDrive 盘实现同步（简而言之这个路径设置为 OneDrive 路径下的 Zotero 文件夹路径，需要先在 OneDrive 文件夹中创建”Zotero 文件夹 “）。  
![](https://i-blog.csdnimg.cn/blog_migrate/ed54b0f5de416cb9a543cd8f7af9500a.png)  
④以管理员身份打开 cmd，输入以下代码将 OneDrive 同步盘中的 zotero 文件夹中的 storage 文件夹链接到数据储存位置中的 storage 文件夹

```
mklink /J "xxxx\Zotero\storage" "xxxx\OneDrive\Zotero\storage"
```

注意：  
1、第一个双引号中的路径填写数据储存文件的路径再加”\storage"，第二个双引号中的路径填写根目录的路径再加”\storage"  
2、在数据储存文件的文件夹下不能有 storage 文件夹，不然无法执行该命令，而根目录下需要新建一个 storage 文件夹

提示：OneDrive 同步盘用学生账号申请可以获得免费的 1T 云空间

#### （2）配置输出文献引用格式

由于 zotero 自带的 “gb-t-7714-2015” 格式存在缺陷，因此需要对其进行自定义，自定义后的文件可以从下面链接获取，下载解压后可以直接使用

> 理工科：  
> https://wwd.lanzouj.com/iUYKH05ujtze  
> 密码: 81be

> 文科：  
> 下载: https://wwd.lanzouj.com/ieF9g05ukh4h  
> 密码: 6fh9

安装步骤如下：  
①下载解压后直接双击安装，若是出现下面的弹窗点击 ok 即可  
![](https://i-blog.csdnimg.cn/blog_migrate/42478aa58bc731428aecd96f95c1f58f.png)  
②安装完成后重启 Zotero 软件就可以在首选项设置的 “导出” 栏看到如下图刚刚安装的参考文献格式，至此中文文献格式安装成功  
![](https://i-blog.csdnimg.cn/blog_migrate/9b5685f7e55f07a1fc0c032458a9e57e.png)

#### （3）Zotero+ Sci-Hub

（参考这篇文章进行设置：[https://zhuanlan.zhihu.com/p/112141757](https://zhuanlan.zhihu.com/p/112141757)）  
①打开 Zotero 的首选项，点击高级–> 设置编辑器  
![](https://i-blog.csdnimg.cn/blog_migrate/423032f6697ff40da7fcc99a0a68c58c.png)  
②搜索`extensions.zotero.findPDFs.resolvers`，如下：  
![](https://i-blog.csdnimg.cn/blog_migrate/e7a73b8eedfbd4237dc5044207502d9c.png)  
删除 []，并将以下代码粘贴进去并点击 ok

```
{
    "name":"Sci-Hub",
    "method":"GET",
    "url":"https://sci-hub.ren/{doi}",
    "mode":"html",
    "selector":"#pdf",
    "attribute":"src",
    "automatic":true
}
```

![](https://i-blog.csdnimg.cn/blog_migrate/835e81c3aa62fd058be417b483da9044.png)  
到此就成功将 Sci-Hub 配置为 PDF 解析器了，也就是说替代了默认的 Unpaywall。

现在，无需重启 Zotero，即可调用 Sci-Hub 免费下载文献了。

如果在网页无法抓取，可以直接用 DOI 下载，将 DOI 复制到下面的输入框中即可成功下载（前提是按照前面的步骤配置 Sci-Hub 为 PDF 解析器）  
![](https://i-blog.csdnimg.cn/blog_migrate/8b7d8971d53f1bfe5937b8bdc57ec376.png)

此部分内容是原理，可以不管

*   在 "url":"https://sci-hub.ren/{doi}" 中，目前可用的域名有. tw、.ren、.si、.shop，大家可以挑选其中一个，哪个用起来体验更好就用哪个。（当然，由于 Sci-Hub 经常更换域名，保不准改天哪个域名就挂了，或者有新的域名出来，因此此处的代码未来也会根据需要进行更新）
*   从 "url":"https://sci-hub.ren/{doi}" 还能看到一点。由于 Sci-Hub 是通过 doi 下载文献的，因此该 PDF 解析器也需要 doi。也就说你的文献必须要有 doi，如果 doi 是空缺的，便无法通过 PDF 解析器免费下载文献。幸运的是，对于缺失 doi 的文献，我们可以通过插件 zotero-shortdoi[5] 插件一键抓取 doi（参考文章 zotero-shortdoi + Sci-Hub，让 99% 的文献都能被免费下载！）。
*   “automatic”:true，如果设置为 true，Zotero 会自动下载保存到 Zotero 中的文献的 PDF。比如你用 Zotero Connector 保存了一些文献到 Zotero，它便会自动帮你从 Sci-Hub 下载文献，并附在相应文献条目下。如果你不需要自动下载，可以设置为 "automatic":false。
*   如果你未开启任何网络加速器，即正常使用网络，可以认为 Find Available PDF 的进度接近你手动从 Sci-Hub 下载文献的速度。大家应该都体验过，不开启加速器的情况下，Sci-Hub 的访问速度还是比较慢的，甚至有时候 PDF 加载不出来。
*   假如你开启了加速器，推荐使用全局代理模式，而不是 PAC 模式，因为两种情况下 Find Available PDF 的进度差异比较大

二、安装 Zotero 常用插件
----------------

文中涉及的 zotero 插件合集，lanzou 云下载链接：

> https://wwd.lanzouj.com/iKgRA05uk2ib  
> 密码: 1rew

### 1、ZotFile 插件（最重要的插件）

软件介绍：  
自动重命名，移动 PDF 并将其附加到 Zotero 项目，将 PDF 从 Zotero 库同步到您的（移动）PDF 阅读器（例如 iPad，Android 平板电脑等）并从 PDF 文件中提取注释。

#### （1）ZotFile 插件下载

点击链接进行下载：[http://zotfile.com/](http://zotfile.com/)

蓝奏云下载链接：

> https://wwd.lanzouj.com/ilnYJxu47ti  
> 密码: epvi

![](https://i-blog.csdnimg.cn/blog_migrate/81f3d64ee40eac2b910e34b5382d01b2.png)

#### （2）ZotFile 插件安装

点击 zotero 工具——插件弹出下面的对话框，将下载好的. xpi 插件拖入该对话框中进行安装![](https://i-blog.csdnimg.cn/blog_migrate/bccefc10400eeb525358f65466d67cd3.png)

#### （3）重启 Zotero

安装后出现如下图界面点击 “Restart now” 重启 Zotero 软件安装完成  
![](https://i-blog.csdnimg.cn/blog_migrate/4199b0ea19640358c6b80635497d463d.png)

#### （4）ZotFile 插件配置

①配置文件储存位置  
这部分主要配置两个位置，一个是文献下载的临时储存路径，该路径可以设置为常用的下载路径，由于下载的文献在重命名后会被移动到下一部分设置的文件实际储存路径中，因此这个路径设置在哪不重要；第二个是重命名后实际文件的储存路径，由于需要多端同步因此这个路径必须设置在 OneDrive 同步盘中，设置为之前建好的`“xxxx\OneDrive\Zotero\storage”`文件夹中；下方的勾是选择是否将重命名后的文献按照列表中的分类分成一个个子文件夹。  
![](https://i-blog.csdnimg.cn/blog_migrate/10ac065b6c68aca5fb3542ef8dbb0f16.png)  
②设置重命名规则  
根据自己的习惯设置重命名规则，这里按照 “年份_题目_作者” 的命名规则可供参考  
![](https://i-blog.csdnimg.cn/blog_migrate/f6b4878247c6a794f66f726f5d877052.png)  
③添加 caj 格式支持（caj 格式文件也可重命名）  
直接在下图框框位置添加 caj 格式  
![](https://i-blog.csdnimg.cn/blog_migrate/0c854c211a03dc4b811e7f7fade1db2a.png)

### 2、Zotero translators 插件

#### （1）Zotero translators 介绍及下载

```
Zotero translators是一款Zotero的中文网页抓取插件，用于维护各种中文翻译器。不安装这个插件会出现无法抓取知网等中文文献元数据。
```

*   [Zotero translators github 下载及使用说明主页](https://github.com/l0o0/translators_CN)。
    
*   GitHub 下载缓慢也可以从这个地方[下载](https://wwi.lanzouj.com/ia2hyxtqnmd)
    

#### （2）Zotero translators 安装

①解压压缩包，可以看到如下图所示的 translators 目录，将该目录中所需的文件复制到 Zotero 的 translators 目录  
![](https://i-blog.csdnimg.cn/blog_migrate/b070a4995f545f8909584251d39000ed.png)  
②从 Zotero 首选项 -> 高级 -> 打开数据文件夹中打开 translators 目录，将上面下载文件中 translators 目录下的所有文件复制到数据文件夹中的 translators 目录下，提示有重复的文件选择替换  
![](https://i-blog.csdnimg.cn/blog_migrate/72bb189700b93803931452c9aea4e190.png)  
![](https://i-blog.csdnimg.cn/blog_migrate/b9c2c53ed08f4f17432d37e883b83cce.png)

#### （3）Zotero translators 插件更新

右击 Connector 插件，点击扩展选项，在 Advanced 界面点击 “Update Translators”，可多点击几次保证更新完成  
![](https://i-blog.csdnimg.cn/blog_migrate/92db64e1e2d524e69909745cc3750cb5.png)  
![](https://i-blog.csdnimg.cn/blog_migrate/567158b53d65b34f19f433ea141edd20.png)

### 3、 Jasminum 插件

#### （1）功能介绍及下载

*   利用 Zotero Connector 直接获取题录及对应 PDF 等附件内容。但是不能满足从 Zotero 软件直接导入中文 PDF 文件的元数据读取需求。  
    Jasminum 就是为了解决这一问题而出现的，具体介绍看 [Jasminum github 官网](https://github.com/l0o0/jasminum)主页。
*   插件可从 [Jasminum github 官网](https://github.com/l0o0/jasminum/releases/tag/v0.1.6)下载. xpi 文件

lanzou 云下载链接：

> 下载: https://wwd.lanzouj.com/iVSaOxu47uj  
> 密码: fnnz

![](https://i-blog.csdnimg.cn/blog_migrate/98f62bec832e9058dc14c966e7af6e3a.png)

#### （2）安装 Jasminum 插件

和上面安装插件过程相同，拖动安装出现如下界面说明安装完成  
![](https://i-blog.csdnimg.cn/blog_migrate/e7db7fc1e52735c81b03a8c0e003b9ed.png)

#### （3）安装 PDFtk server

若想使用 Jasminum 的书签添加功能，需要提前安装好 PDFtk server

*   [下载](https://www.pdflabs.com/tools/pdftk-server/)  
    ![](https://i-blog.csdnimg.cn/blog_migrate/714f5dd932ee6322c0f41cfd74dad083.png)
    
*   安装：正常安装到自定义位置即可（需要记住自己安装的位置）
    

#### （4）配置 Jasminum 插件

该插件安装完成后会在 Zotero 首选项配置中出现茉莉花图标，点击该图标后再配置 PDFtk server 安装目录如下图所示，配置完成后即可使用  
![](https://i-blog.csdnimg.cn/blog_migrate/ba16f41e424fbe50d87cfa3722d48468.png)

#### （5）Jasminum 使用

Jasminum 插件配合 PDFtk server 主要有三个功能

一是可以使用该插件抓取中文文献的元数据，如将下载好的文献拖入可以直接右击查找元数据  
![](https://i-blog.csdnimg.cn/blog_migrate/c8430944bd4742d738bce41a29ca0450.png)  
二是可以生成 PDF 的目录（一般下载学位论文的 PDF 版本是没有目录的）  
![](https://i-blog.csdnimg.cn/blog_migrate/5df7faaf67650d93112dec5794190580.png)  
注意：如果不想下载知网的 CAJ 格式可以访问[知网海外中文版](https://chn.oversea.cnki.net/index/singleTheme.html?subjectId=6)

三是可以将作者姓名进行合并  
![](https://i-blog.csdnimg.cn/blog_migrate/04c945aa922356d7ab50ff0ade891eae.png)

### 4、Zotero IF 插件（Zotero IF v1.10）

（from：[青柠学术](https://mp.weixin.qq.com/s/e5qJVzLwAiHWjHkc2oHwjw)）

下载链接：

```
下载:https://wwi.lanzouj.com/ij7eu0076sli 
密码:9sii
```

安装步骤及使用：  
1）下载链接中的文件并解压  
2）进入 Zotero 菜单 Tools–>Add-ons，点击右上角小齿轮，然后点击 Install add-on from file…，选择 zotero-if.xpi 插件，完成安装  
3）重启 Zotero 后调出 “馆藏目录” 和“索取号”，分别对应中科院分区和影响因子（JCR IF 只针对 SCI 期刊论文）  
![](https://i-blog.csdnimg.cn/blog_migrate/44d750ce17300cc473cac94da33ebb73.png)

4）选中要查询的论文（可多选）右击 “Update If(s)” 即可更新

### 5、 delitemwithatt 插件

（github 下载链接：[https://github.com/redleafnew/delitemwithatt/releases](https://github.com/redleafnew/delitemwithatt/releases)）

lanzou 云下载链接：

```
下载:https://wwd.lanzouj.com/iwvKd024dbkb 
密码:e8ak
```

功能：  
1. 删除条目或分类的同时将链接的附件也一块删除  
2. 导出附件  
（两个非常实用的功能）  
![](https://i-blog.csdnimg.cn/blog_migrate/8b0bf8e9ee74f8a70d41d29bfd2029fa.png)

### 6、zotero-pdf-translate 插件（内置阅读器划线翻译插件）

（github 链接：[https://github.com/windingwind/zotero-pdf-translate](https://github.com/windingwind/zotero-pdf-translate)）

lanzou 云下载链接：

```
下载:https://wwd.lanzouj.com/iJrTa024dblc 
密码:dfn5
```

功能：内置多种翻译引擎可以在通过 zotero 内置翻译器打开后直接进行画线翻译  
![](https://i-blog.csdnimg.cn/blog_migrate/d3d747ffb6baf549e70e2ccabb085cae.png)

### 7、zotero-doi-manager 插件（自动获取 doi）

（github 链接：[https://github.com/bwiernik/zotero-shortdoi/releases](https://github.com/bwiernik/zotero-shortdoi/releases)）

lanzou 云下载链接（v1.4.2）：

```
下载:https://wwd.lanzouj.com/iI5Lb04j22kd 
密码:a5z0
```

该插件自动获取期刊文章的 DOI 名称，以及使用 [http://shortdoi.org](http://shortdoi.org) 查找 shortDOI 名称。该加载项还会验证存储的 DOI 是否有效，并标记无效的 DOI。

插件功能：

*   获取 shortDOI：对于所选项目，查找 shortDOI（替换存储的 DOI，如果有）并标记无效的 DOI。
*   获取长 DOI：对于所选项目，查找完整的 DOI（替换存储的 DOI，如果有）并标记无效的 DOI。
*   验证并清理 DOI：对于所选项目，查找完整的 DOI（替换存储的 DOI，如果有），验证存储的 DOI 是否有效，并标记无效的 DOI。
*   此函数还会从 DOI 字段中删除不必要的前缀（如：发布者 URL 前缀）。  
    ![](https://i-blog.csdnimg.cn/blog_migrate/0daac5c7c9b9a1dac7750cef477502d2.png)

### 8、zotero-reference 插件（自动获取参考文献）

（github 链接：[https://github.com/MuiseDestiny/zotero-reference](https://github.com/MuiseDestiny/zotero-reference)）

lanzou 云下载链接（v0.5.8）：

```
下载:https://wwal.lanzoue.com/i55J511qv7ob 
密码:8m82
```

![](https://i-blog.csdnimg.cn/blog_migrate/26bcd763d8002ebb8587edce5930cec2.png)

*   单击蓝色区域 -> 复制此条参考文献信息；
    
*   ctrl + 单击蓝色区域 -> 用默认浏览器打开文献地址；
    
*   单击 + -> 添加参考文献至正在阅读文献所在文件夹下并与之双向关联；
    
*   ctrl + 单击 + -> 添加参考文献至当前所在文件夹下并与之双向关联；
    

如有需要可以加入 QQ 群大家相互交流学习：784535340 / 608998794

与 zotero 配合使用的笔记软件：  
[最新 zotero 与 obsidian 联动教程（可代替 citations 和 mdnotes）](https://blog.csdn.net/qq_43309940/article/details/125150487)

> 参考：  
> [https://zhuanlan.zhihu.com/p/408027026](https://zhuanlan.zhihu.com/p/408027026)  
> [https://zhuanlan.zhihu.com/p/112141757](https://zhuanlan.zhihu.com/p/112141757)  
> [https://zhuanlan.zhihu.com/p/104848524](https://zhuanlan.zhihu.com/p/104848524)  
> [https://blog.csdn.net/qq_43210428/article/details/120377475](https://blog.csdn.net/qq_43210428/article/details/120377475)  
> [https://mp.weixin.qq.com/s/e5qJVzLwAiHWjHkc2oHwjw](https://mp.weixin.qq.com/s/e5qJVzLwAiHWjHkc2oHwjw)