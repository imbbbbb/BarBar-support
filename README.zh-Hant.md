<div align="center">

<img src="icon.png" width="128" alt="BarBar">

# BarBar

**把 Mac 選單列收拾乾淨。**

[下載最新版](https://github.com/imbbbbb/BarBar-support/releases/latest) ·
[回報問題](https://github.com/imbbbbb/BarBar-support/issues/new/choose) ·
[隱私權政策](PRIVACY.zh-Hant.md)

[简体中文](README.md) · **繁體中文** · [English](README.en.md)

<a href="https://ko-fi.com/P4W31ZZFU0">
  <img src="https://img.shields.io/badge/%E5%9C%A8%20Ko--fi%20%E4%B8%8A%E6%94%AF%E6%8C%81%E6%88%91-72a4f2?style=for-the-badge&logo=ko-fi&logoColor=white" alt="在 Ko-fi 上支持我" height="36">
</a>

</div>

---

選單列圖像越裝越多，想找的那個反而被擠不見了。**BarBar** 是專為 macOS 27 原生開發的選單列整理工具——把不常用的圖像收起來，需要時點一下（或滑鼠移上去）就出來。

## 怎麼用

**1. 拖放分組**

打開設定，把應用程式圖像拖進對應的分組即可：

- **常駐顯示**：一直留在選單列上。
- **隱藏**：平時收起，需要時再展開。
- **永久隱藏**：徹底不在選單列顯示（拖回其他分組並重新啟動該軟體即可復原）。

**2. 隨手展開**

點一下選單列上的 BarBar 圖像、開啟**滑鼠停留自動展開**，或按快速鍵（預設 <kbd>⌥</kbd><kbd>⌘</kbd><kbd>B</kbd>）。提供兩種展開方式：

- **下方面板**：在選單列下方彈出原生毛玻璃面板，支援左鍵點按、右鍵選單，按住圖像就能直接拖曳排順序。
- **就地展開**：直接在選單列原位鋪開，可設定滑鼠移開後自動收合。

還可以自選 4 種控制圖像樣式（箭頭 / 直線 / 圓點 / 刪節號）。日常背景執行不擷取畫面、不連網收集任何資料，詳見[隱私權政策](PRIVACY.zh-Hant.md)。

## 安裝

系統需求：**macOS 27 以上**。

1. 下載最新 [DMG 安裝檔](https://github.com/imbbbbb/BarBar-support/releases/latest)，把 **BarBar** 拖進「**應用程式**」檔案夾（請勿直接在 DMG 視窗內點兩下執行）；
2. 第一次打開時，在「應用程式」裡**按右鍵點 BarBar → 打開**，之後即可正常點兩下啟動；
3. 依提示開啟**輔助使用**權限（用於辨識選單列上有哪些圖像；**螢幕錄製**為選用權限，不開啟也不影響正常使用）。

<details>
<summary>提示「已損毀，應移到垃圾桶」怎麼辦？</summary>

因為尚未購買 Apple 開發者公證，部分系統下載後會擋下。打開「終端機」貼上並執行下面這一行即可正常開啟：

```bash
xattr -dr com.apple.quarantine /Applications/BarBar.app
```

</details>

## 常見問題與系統限制

- **找不到 BarBar 圖像了？** 按 <kbd>⌥</kbd><kbd>⌘</kbd><kbd>B</kbd> 就能立刻找回並打開設定。想調整選單列上常駐圖像的前後順序，按住 <kbd>⌘</kbd> 直接在選單列上拖曳即可（別拖到選單列外面放手）。
- **右上角點時間打不開通知中心？** 當「隱藏」組裡有圖像時，受 macOS 底層隱藏機制限制，通知中心會暫時停用；如果只用「常駐顯示」和「永久隱藏」則不受影響（[#4](https://github.com/imbbbbb/BarBar-support/issues/4)）。
- **個別軟體的圖像沒放進隱藏組也消失了？** 請確認該軟體安裝在「應用程式」（`/Applications`）檔案夾下。從其他目錄啟動的軟體，在隱藏開啟期間會被 macOS 系統自動收走。
- **系統內建圖像怎麼藏？** 輸入法、Spotlight、Siri 可直接在 BarBar 裡分組；時鐘、Wi-Fi、控制中心等核心圖像請在「系統設定 → 選單列」裡開關。
- **同一個軟體有多個選單列圖像？** 系統依軟體整體控制顯示與隱藏，同一軟體的多個圖像會一起收起或展開。

## 回報與關於

遇到 Bug 或有功能建議，歡迎直接開 [Issue](https://github.com/imbbbbb/BarBar-support/issues/new/choose)。回報問題時附上「設定 → 關於 → 匯出診斷資訊」產生的文字，能幫我更快找出原因。

BarBar 是一款從零獨立編寫的閉源軟體，本儲存庫僅用於安裝檔發佈與問題回報。
