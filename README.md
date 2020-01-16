## Android应用《离线全唐诗》

设计目的：利用碎片化时间，无障碍欣赏唐诗。这个应用是我自用的。  
[点击这里](https://github.com/animalize/QuanTangshi/releases)下载编译好的.apk安装文件，需要Android 4.1+。

### 特性
1.  离线全唐诗数据库，有5万余首唐诗。  
2.  支持繁体、简体切换。（注：原始数据为繁体字）  
3.  学习功能，点击几下就可以搜索唐诗里的古代词汇、典故，让您无障碍欣赏唐诗。  
4.  标签功能，可以给诗打标签，并通过标签进行检索。

### 截图
<table>
<tr>
<td>阅读</td><td>学习功能</td><td>学习功能</td><td>最近列表</td>
</tr>
<tr>
<td><img src="https://raw.githubusercontent.com/animalize/pics/master/QuanTangshi/1.png" /></td>
<td><img src="https://raw.githubusercontent.com/animalize/pics/master/QuanTangshi/2.png" /></td>
<td><img src="https://raw.githubusercontent.com/animalize/pics/master/QuanTangshi/3.png" /></td>
<td><img src="https://raw.githubusercontent.com/animalize/pics/master/QuanTangshi/4.png" /></td>
</tr>
<td>标签功能</td><td>标签搜索</td><td>标签管理</td><td>阅读设置</td>
</tr>
<tr>
<td><img src="https://raw.githubusercontent.com/animalize/pics/master/QuanTangshi/5.png" /></td>
<td><img src="https://raw.githubusercontent.com/animalize/pics/master/QuanTangshi/6.png" /></td>
<td><img src="https://raw.githubusercontent.com/animalize/pics/master/QuanTangshi/7.png" /></td>
<td><img src="https://raw.githubusercontent.com/animalize/pics/master/QuanTangshi/8.png" /></td>
</tr>
</table>

### 编译指南
需要生成全唐诗的SQLite数据库文件，步骤如下：
1.  下载原始的[全唐诗数据](https://github.com/animalize/chinese-poetry)，此为json格式。（请从这里的链接下载，这里会持续修订数据。）
2.  给电脑安装Python 3.x
3.  把tools目录下的`ok_make_db.py`文件放到全唐诗数据目录下，双击此脚本生成`tangshi.db.zip`文件。
4.  把生成的`tangshi.db.zip`放到`\app\src\main\assets\databases`目录下，此时需要手工创建databases目录

（在修订全唐诗数据后，仅需递增MyAssetsDatabaseHelper.java文件里的DATABASE_VERSION变量，就可以在安装后首次运行APP时更新全唐诗数据库）

### 感谢
使用了jackeyGao网友整理的全唐诗数据库：  
https://github.com/chinese-poetry/chinese-poetry

参考了OpenCC提供的繁体->简体转换表：  
https://github.com/BYVoid/OpenCC

使用的其它开源项目：[标签控件](https://github.com/whilu/AndroidTagView)，[底部向上拖动控件](https://github.com/hannesa2/AndroidSlidingUpPanel)，[assets数据库支持](https://github.com/jgilfelt/android-sqlite-asset-helper) 。
