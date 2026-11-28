<div align="center">

<img src="icon.png" width="128" alt="BarBar">

# BarBar

**把 Mac 菜单栏收拾干净。**

[下载最新版](https://github.com/imbbbbb/BarBar-support/releases/latest) ·
[反馈问题](https://github.com/imbbbbb/BarBar-support/issues/new/choose) ·
[隐私政策](PRIVACY.md)

**简体中文** · [繁體中文](README.zh-Hant.md) · [English](README.en.md)

<a href="https://ko-fi.com/P4W31ZZFU0">
  <img src="https://img.shields.io/badge/%E5%9C%A8%20Ko--fi%20%E4%B8%8A%E6%94%AF%E6%8C%81%E6%88%91-72a4f2?style=for-the-badge&logo=ko-fi&logoColor=white" alt="在 Ko-fi 上支持我" height="36">
</a>

</div>

---

菜单栏图标越装越多，想找的那个反而被挤没了。**BarBar** 是专为 macOS 27 原生开发的菜单栏整理工具——把不常用的图标收起来，用的时候点一下（或者鼠标移上去）就出来。

## 怎么用

**1. 拖放分组**

打开设置，把应用图标拖进对应的分组即可：

- **常显**：一直留在菜单栏上。
- **隐藏**：平时收起，需要时再展开。
- **永久隐藏**：彻底不在菜单栏显示（移回其他分组并重启该软件即可恢复）。

**2. 随手展开**

点击菜单栏上的 BarBar 图标、开启**鼠标悬停自动展开**，或按快捷键（默认 <kbd>⌥</kbd><kbd>⌘</kbd><kbd>B</kbd>）。提供两种展开方式：

- **下方面板**：在菜单栏下方弹出原生毛玻璃面板，支持左键点击、右键菜单，按住图标就能直接拖动排顺序。
- **本行展开**：直接在菜单栏原位铺开，可设置鼠标移开后自动收起。

还可以自选 4 种控制图标样式（箭头 / 竖线 / 圆点 / 省略号）。日常后台运行不截屏、不联网收集任何数据，详见[隐私政策](PRIVACY.md)。

<a id="install"></a>

## 安装

系统要求：**macOS 27 及以上**。

1. 下载最新 [DMG 安装包](https://github.com/imbbbbb/BarBar-support/releases/latest)，把 **BarBar** 拖进「**应用程序**」文件夹（请勿直接在 DMG 窗口内双击运行）；
2. 第一次打开时，在「应用程序」里**右键点击 BarBar → 打开**，之后即可正常双击启动；
3. 按提示开启**辅助功能**权限（用于识别菜单栏上有哪些图标；**屏幕录制**为可选权限，不开启也不影响正常使用）。

<details>
<summary>提示「已损坏，应移到废纸篓」怎么办？</summary>

因为尚未购买 Apple 开发者公证，部分系统下载后会拦截。打开「终端」粘贴运行下面这一行即可正常打开：

```bash
xattr -dr com.apple.quarantine /Applications/BarBar.app
```

</details>

<a id="faq"></a>

## 常见问题与系统限制

- **找不到 BarBar 图标了？** 按 <kbd>⌥</kbd><kbd>⌘</kbd><kbd>B</kbd> 就能立刻找回并打开设置。想调整菜单栏上常显图标的前后顺序，按住 <kbd>⌘</kbd> 直接在菜单栏上拖动即可（别拖到菜单栏外面松手）。
- **右上角点时间打不开通知中心？** 当「隐藏」组里有图标时，受 macOS 底层隐藏机制限制，通知中心会暂时停用；如果只用「常显」和「永久隐藏」则不受影响（[#4](https://github.com/imbbbbb/BarBar-support/issues/4)）。
- **个别软件的图标没放进隐藏组也消失了？** 请确保该软件安装在「应用程序」（`/Applications`）文件夹下。从其他目录启动的软件，在隐藏开启期间会被 macOS 系统自动收走。
- **系统自带图标怎么藏？** 输入法、Spotlight、Siri 可直接在 BarBar 里分组；时钟、Wi-Fi、控制中心等核心图标请在「系统设置 → 菜单栏」里开关。
- **同一个软件有多个菜单栏图标？** 系统按软件整体控制显隐，同一软件的多个图标会一起收起或展开。

## 反馈与关于

遇到 Bug 或有功能建议，欢迎直接提 [Issue](https://github.com/imbbbbb/BarBar-support/issues/new/choose)。反馈问题时附上「设置 → 关于 → 导出诊断信息」生成的文本，能帮我更快定位原因。

BarBar 是一款从零独立编写的闭源软件，本仓库仅用于安装包分发与问题反馈。
