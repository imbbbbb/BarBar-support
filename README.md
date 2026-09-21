<div align="center">

<img src="icon.png" width="128" alt="BarBar">

# BarBar

**把菜单栏收拾干净。**

[下载最新版](https://github.com/imbbbbb/BarBar-support/releases/latest) ·
[反馈问题](https://github.com/imbbbbb/BarBar-support/issues/new/choose)

**简体中文** · [繁體中文](README.zh-Hant.md) · [English](README.en.md)

<a href="https://ko-fi.com/P4W31ZZFU0">
  <img src="https://img.shields.io/badge/%E5%9C%A8%20Ko--fi%20%E4%B8%8A%E6%94%AF%E6%8C%81%E6%88%91-72a4f2?style=for-the-badge&logo=ko-fi&logoColor=white" alt="在 Ko-fi 上支持我" height="38">
</a>

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
2. 打开后把 BarBar 拖进「应用程序」；
3. **退出 dmg 窗口，从「应用程序」里打开 BarBar**；
4. 第一次打开要右键点图标 →「打开」，在弹出的对话框里再点一次「打开」。
   之后就能正常双击了。

> [!IMPORTANT]
> **不要直接从 dmg 窗口里双击运行。**
>
> 从浏览器下载的 app 带「隔离」标记，直接运行时 macOS 会把它搬到一个临时位置
> （App Translocation）。在那个位置系统不认 BarBar 的身份，隐藏功能会失灵 ——
> 0.1 版在这种情况下会把自己的箭头一起藏掉，菜单栏上什么都不剩。
>
> 0.1.1 起 BarBar 会检测到这种情况，拒绝隐藏并提示你先安装，但**正确的做法始终是
> 先拖进「应用程序」再打开**。

系统要求：**macOS 27 及以上**。隐藏菜单栏图标依赖 macOS 27 引入的系统机制，
更早的版本上做不到。

<details>
<summary>为什么要右键打开？</summary>

BarBar 目前没有做 Apple 的开发者签名和公证，所以 macOS 会拦一下。右键打开是系统
给未公证软件留的正规入口，不是绕过安全机制 —— 你依然是在明确地授权这一个 app。

如果双击后提示「已损坏，应移到废纸篓」，那是隔离属性在作祟，终端里跑一句：

```
xattr -dr com.apple.quarantine /Applications/BarBar.app
```

</details>

首次运行会请求**辅助功能**权限 —— 用来读出菜单栏上有哪些图标。隐藏功能本身不需要
任何权限。「下方面板」形态如果要显示图标的样子，还需要**屏幕录制**权限；不给也能用，
只是面板里显示为名字。

BarBar 不收集任何信息，也没有服务器。这两个权限具体用在哪、每天一次的检查更新到底发了
什么，都写在[隐私政策](PRIVACY.md)里。

## 万一箭头不见了

按 <kbd>⌥</kbd><kbd>⌘</kbd><kbd>B</kbd>。箭头不在菜单栏上时，这个快捷键会把它拉回来
并打开设置窗口。

箭头会消失通常是因为按住 <kbd>⌘</kbd> 拖动时松手松在了菜单栏外面 —— macOS 会把状态项
当成「用户不想要了」，而且这个决定会一直记着。0.1.1 起 BarBar 每次启动都会把它恢复。

## 现在还做不到

坦白讲清楚，省得你试半天：

- **箭头的位置、常显图标的排序，BarBar 控制不了。** 系统没有提供排序的接口。
  想调整顺序，按住 <kbd>⌘</kbd> 直接在菜单栏上拖 —— 这是 macOS 自己的功能。
  拖的时候注意别松手在菜单栏外面，那会让图标消失。
- **隐藏的粒度是「应用」，不是「图标」。** 同一个 app 放了好几个图标的话，
  只能一起藏、一起显。
- 少数图标系统不允许隐藏，BarBar 会在设置里把它们标出来。

## 反馈

这个仓库就是干这个的。遇到问题、想要什么功能，都开
[Issue](https://github.com/imbbbbb/BarBar-support/issues/new/choose)。

报 bug 时麻烦带上 macOS 版本、BarBar 版本，以及是哪个 app 的图标出的问题。

## 支持开发

如果 BarBar 帮你把菜单栏收拾清爽了，可以请我喝杯咖啡。

<a href="https://ko-fi.com/P4W31ZZFU0">
  <img src="https://img.shields.io/badge/%E5%9C%A8%20Ko--fi%20%E4%B8%8A%E6%94%AF%E6%8C%81%E6%88%91-72a4f2?style=for-the-badge&logo=ko-fi&logoColor=white" alt="在 Ko-fi 上支持我" height="38">
</a>

不支持也完全没关系，提个 Issue 说说哪里不好用，一样有价值。

## 关于源码

BarBar 是闭源软件，这个仓库只负责分发和收集反馈，不包含源代码。

它从零写起，没有复用任何现成项目的代码。
