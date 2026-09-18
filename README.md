<div align="center">

<img src="icon.png" width="128" alt="BarBar">

# BarBar

**把菜单栏收拾干净。**

[下载最新版](https://github.com/imbbbbb/BarBar-support/releases/latest) ·
[反馈问题](https://github.com/imbbbbb/BarBar-support/issues/new/choose)

</div>

---

菜单栏图标越攒越多，挤到最后自己要找的那个反而看不见了。BarBar 让你决定谁常显、
谁收起来，收起来的那些点一下箭头就出来。

原生编写，不需要辅助功能或屏幕录制权限就能隐藏图标。

## 两件事

**一、挑图标。** 在设置里勾选哪些常显、哪些收起。

**二、展开。** 点菜单栏上的箭头，或者按 <kbd>⌥</kbd><kbd>⌘</kbd><kbd>B</kbd>。
展开形态有两种，自己选：

- **原地展开** —— 收起的图标在菜单栏那一行里就地铺开；
- **下方面板** —— 在菜单栏底下弹一个面板，图标摆在里面。

## 安装

1. 从 [Releases](https://github.com/imbbbbb/BarBar-support/releases/latest) 下载 dmg；
2. 打开后把 BarBar 拖进「应用程序」。

> **必须装在「应用程序」文件夹里。** 放在别处时系统不认 BarBar 自己的身份，
> 会把它自己的箭头也一起藏掉。

首次运行会请求**辅助功能**权限 —— 用来读出菜单栏上有哪些图标。隐藏功能本身不需要
任何权限。「下方面板」形态如果要显示图标的样子，还需要**屏幕录制**权限；不给也能用，
只是面板里显示为名字。

系统要求：macOS 14 及以上。

## 现在还做不到

坦白讲清楚，省得你试半天：

- **箭头的位置、常显图标的排序，BarBar 控制不了。** 系统没有提供排序的接口。
  想调整顺序，按住 <kbd>⌘</kbd> 直接在菜单栏上拖 —— 这是 macOS 自己的功能。
- **隐藏的粒度是「应用」，不是「图标」。** 同一个 app 放了好几个图标的话，
  只能一起藏、一起显。
- 少数图标系统不允许隐藏，BarBar 会在设置里把它们标出来。

## 反馈

这个仓库就是干这个的。遇到问题、想要什么功能，都开
[Issue](https://github.com/imbbbbb/BarBar-support/issues/new/choose)。

报 bug 时麻烦带上 macOS 版本、BarBar 版本，以及是哪个 app 的图标出的问题。

## 关于源码

BarBar 是闭源软件，这个仓库只负责分发和收集反馈，不包含源代码。

它从零写起，没有复用任何现成项目的代码。
