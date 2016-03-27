# PulltoRefresh 下拉刷新
Copy Right &copy; 2016 Aurora Studio.

## Desicription 介绍

This is a simple CustomControl to enable pull to refresh on Universal Windows apps.
这是适用于通用 Windows 平台的简易下拉刷新控件。

Based on ScrollViewer, auto detect and enable, and it can be force enabled.
基于 SrollViewer 修改而来，自动检测是否支持(使用触摸屏或移动设备就开启)，也可以强制开启。

This is the very first version, and will be continuously updated
这是最初版本，将会持续更新

## Features 特性

 - 使用 ManipulationDelta 作为交互控制方式
 - 交互与 ScrollViewer 大致相同，但不支持横向滚动
 - 从 ContentControl 继承，同时内置了 LayoutUpdated 事件和 VerticalOffset 属性(与 ScrollViewer 一致)
 - 头部是 ProgressRing，刷新时为活动状态，刷新完毕便隐藏并滚回最顶部
 - 头部拥有 Fixed Header 和 Overlay 两种显示方式

## Usage 用法

When you use it in xaml, first add this project as a reference, and write this in xaml:
在一般的项目里，先添加引用，然后在 Page 里添加这条:

    <Page
        ...
        xmlns:ptr ="using:Com.Aurora.Shared.Controls"
        ...
        >
    

then when you want to use it, write this:
当你想使用这个控件的时候，使用下面的方式:

    <ptr:PulltoRefresh VerticalAlignment=...
                       VerticalOffset=... IndicatorDisplayMode=...
                       ForceEnabled=...>
        <!-- Content Here -->
    </ptr:PulltoRefresh>

*ForceEnabled 为 true 时强制开启下拉刷新*
*IndicatorDisplayMode 为枚举值 Header, Overlay 两者之一*

**We are looking forward to your tests and feedbacks**
**我们欢迎你来进行测试**
