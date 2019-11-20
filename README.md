# 色卡

在UI设计中，色彩更多被用在情感渲染、产品价值和信任度定位等方面。通过不同颜色的搭配，UI色彩的感受比文字更能直接影响用户的情绪。

例如KFC和麦当劳，他们的品牌、app甚至都有大面积的红色（红色更能吸引注意，引发刺激、食欲、饥饿），在兰博基尼、宝马、奔驰的网站，能看到更多的黑色（黑色正确使用是能传达出魅力、成熟和奢华）。还有最具信任感的蓝色，作为成熟、稳重的代表色，在fb、twitter、ios等场景都有使用。

因此在我们App开发过程中，色彩的正确使用能提高产品价值、辅助产品定位、影响用户体验情绪。而为了开发中更统一的使用颜色达到产品化的效果，就需要制定一套适合的色卡。

## 基础色卡

[点击查看完整色卡](https://handy045.com/resource/HandyFrame/HandyBasicUI/colors_hdb.html)

![](http://cos.handy045.com/blog/2019-11-06-colors_hdb.jpg)

## 谷歌Material Design色卡

[点击查看完整色卡](https://handy045.com/resource/HandyFrame/HandyBasicUI/colors_google.html)

![](http://cos.handy045.com/blog/2019-11-06-colors_google.jpg)

## Web色卡

[点击查看完整色卡](https://handy045.com/resource/HandyFrame/HandyBasicUI/colors_web.html)

![](http://cos.handy045.com/blog/2019-11-06-colors_web.jpg)

## 色卡XML文件

右键下载链接文件 -> [[colors.xml](https://handy045.com/resource/HandyFrame/HandyBasicUI/colors.xml)]

# 尺寸

## 基础字体尺寸

### 导航栏标题 

```xml
<dimen name="hd_h1">@dimen/hd_sp16</dimen>
```

### 列表标题、主要内容 

```xml
<dimen name="hd_h2">@dimen/hd_sp14</dimen>
```

### 次要内容、二级标题 

```xml
<dimen name="hd_h3">@dimen/hd_sp12</dimen>
```

### 深色背景上提示内容 

```xml
<dimen name="hd_h4">@dimen/hd_sp10</dimen>
```

## 谷歌Material Design字体、边距尺寸

### Default FontSize 字体大小

```xml
<dimen name="google_font_least">@dimen/hd_sp8</dimen>
<dimen name="google_font_micro">@dimen/hd_sp10</dimen>
<dimen name="google_font_small">@dimen/hd_sp12</dimen>
<dimen name="google_font_medium">@dimen/hd_sp14</dimen>
<dimen name="google_font_slarge">@dimen/hd_sp16</dimen>
<dimen name="google_font_large">@dimen/hd_sp18</dimen>
<dimen name="google_font_xlarge">@dimen/hd_sp20</dimen>
<dimen name="google_font_xxlarge">@dimen/hd_sp22</dimen>
```

### Default Margin/Padding 间距大小

```xml
<dimen name="google_spacing_least">@dimen/hd_dp2</dimen>
<dimen name="google_spacing_micro">@dimen/hd_dp4</dimen>
<dimen name="google_spacing_small">@dimen/hd_dp6</dimen>
<dimen name="google_spacing_medium">@dimen/hd_dp8</dimen>
<dimen name="google_spacing_slarge">@dimen/hd_dp10</dimen>
<dimen name="google_spacing_large">@dimen/hd_dp12</dimen>
<dimen name="google_spacing_xlarge">@dimen/hd_dp16</dimen>
<dimen name="google_spacing_xxlarge">@dimen/hd_dp18</dimen>
```

## 通用尺寸

更多通用尺寸请在[尺寸XML](#尺寸XML文件)文件中查看

![](http://cos.handy045.com/blog/2019-11-07-dimen_default.jpg)

## 尺寸XML文件

右键下载链接文件 -> [[dimens.xml](https://handy045.com/resource/HandyFrame/HandyBasicUI/dimens.xml)]

# 屏幕适配

由于Android系统的开放性，任何用户、开发者、OEM厂商、运营商都可以对Android进行定制，于是导致：Android系统碎片化、Android机型屏幕尺寸碎片化、Android屏幕分辨率碎片化。

当Android系统、屏幕尺寸、屏幕密度出现碎片化的时候，就很容易出现同一元素在不同手机上显示不同的问题。于是，我们便需要对Android屏幕进行适配。

国内有关屏幕适配的方案众多，但结合Android系统的特性，我们将使用最小宽度限定符来适配不同屏幕

## 原理

最小宽度限定符适配，通俗点说就是以一个屏幕宽度尺寸为标准，通过与不同屏幕宽度的比例动态设置布局及控件的大小。

## 实现

通过[ScreenMatch](https://plugins.jetbrains.com/plugin/10058-screenmatch)插件，在res文件夹下将dimens.xml内的尺寸生成不同屏幕宽度的xml文件。具体操作过程请参考[wildma - 一种非常好用的Android屏幕适配](https://www.jianshu.com/p/1302ad5a4b04)

## 使用

在平常布局文件配置时，不能再用系统默认的1dp，而是要使用hdp_1dp、hdp_1sp、hdp_h1或google_font/spacing_slarge。

# 相关链接

[中国传统色彩](http://color.uisdc.com)

[Material Design](https://material.io)

[Material Design Colors](https://www.materialui.co/colors)

[wildma - 一种非常好用的Android屏幕适配](https://www.jianshu.com/p/1302ad5a4b04)
