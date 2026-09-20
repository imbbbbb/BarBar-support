<div align="center">

<img src="icon.png" width="128" alt="BarBar">

# BarBar

**把選單列收拾乾淨。**

[下載最新版](https://github.com/imbbbbb/BarBar-support/releases/latest) ·
[回報問題](https://github.com/imbbbbb/BarBar-support/issues/new/choose)

[简体中文](README.md) · **繁體中文** · [English](README.en.md)

<a href="https://ko-fi.com/P4W31ZZFU0">
  <img src="https://img.shields.io/badge/%E5%9C%A8%20Ko--fi%20%E4%B8%8A%E6%94%AF%E6%8C%81%E6%88%91-72a4f2?style=for-the-badge&logo=ko-fi&logoColor=white" alt="在 Ko-fi 上支持我" height="38">
</a>

</div>

---

選單列圖像越攢越多，擠到最後自己要找的那個反而看不見了。BarBar 讓你決定誰常駐顯示、
誰收起來，收起來的那些點一下箭頭就出來。

原生編寫，不需要輔助使用或螢幕錄製權限就能隱藏圖像。

## 兩件事

**一、挑圖像。** 在設定裡勾選哪些常駐顯示、哪些收起。

**二、展開。** 點選單列上的箭頭，或者按 <kbd>⌥</kbd><kbd>⌘</kbd><kbd>B</kbd>。
展開形式有兩種，自己選：

- **就地展開** —— 收起的圖像在選單列那一行裡就地鋪開；
- **下方面板** —— 在選單列底下彈一個面板，圖像擺在裡面。

## 安裝

1. 從 [Releases](https://github.com/imbbbbb/BarBar-support/releases/latest) 下載 dmg；
2. 打開後把 BarBar 拖進「應用程式」；
3. **關掉 dmg 視窗，從「應用程式」裡打開 BarBar**；
4. 第一次打開要按右鍵點圖像 →「打開」，在彈出的對話框裡再點一次「打開」。
   之後就能正常點兩下了。

> [!IMPORTANT]
> **不要直接從 dmg 視窗裡點兩下執行。**
>
> 從瀏覽器下載的 App 帶「隔離」標記，直接執行時 macOS 會把它搬到一個暫存位置
> （App Translocation）。在那個位置系統不認 BarBar 的身分，隱藏功能會失靈 ——
> 0.1 版在這種情況下會把自己的箭頭一起藏掉，選單列上什麼都不剩。
>
> 0.1.1 起 BarBar 會偵測到這種情況，拒絕隱藏並提示你先安裝，但**正確的做法始終是
> 先拖進「應用程式」再打開**。

系統需求：**macOS 27 以上**。隱藏選單列圖像依賴 macOS 27 引入的系統機制，
更早的版本上做不到。

<details>
<summary>為什麼要按右鍵打開？</summary>

BarBar 目前沒有做 Apple 的開發者簽章和公證，所以 macOS 會擋一下。按右鍵打開是系統
給未公證軟體留的正規入口，不是繞過安全機制 —— 你依然是在明確地授權這一個 App。

如果點兩下後提示「已損毀，應移到垃圾桶」，那是隔離屬性在作祟，終端機裡跑一句：

```
xattr -dr com.apple.quarantine /Applications/BarBar.app
```

</details>

首次執行會請求**輔助使用**權限 —— 用來讀出選單列上有哪些圖像。隱藏功能本身不需要
任何權限。「下方面板」形式如果要顯示圖像的樣子，還需要**螢幕錄製**權限；不給也能用，
只是面板裡顯示為名字。

BarBar 不收集任何資訊，也沒有伺服器。這兩個權限具體用在哪、每天一次的檢查更新到底送了
什麼，都寫在[隱私權政策](PRIVACY.zh-Hant.md)裡。

## 萬一箭頭不見了

按 <kbd>⌥</kbd><kbd>⌘</kbd><kbd>B</kbd>。箭頭不在選單列上時，這個快速鍵會把它拉回來
並打開設定視窗。

箭頭會消失通常是因為按住 <kbd>⌘</kbd> 拖曳時放手放在了選單列外面 —— macOS 會把狀態項目
當成「使用者不想要了」，而且這個決定會一直記著。0.1.1 起 BarBar 每次啟動都會把它復原。

## 現在還做不到

坦白講清楚，省得你試半天：

- **箭頭的位置、常駐圖像的排序，BarBar 控制不了。** 系統沒有提供排序的介面。
  想調整順序，按住 <kbd>⌘</kbd> 直接在選單列上拖 —— 這是 macOS 自己的功能。
  拖的時候注意別放手在選單列外面，那會讓圖像消失。
- **隱藏的粒度是「應用程式」，不是「圖像」。** 同一個 App 放了好幾個圖像的話，
  只能一起藏、一起顯示。
- 少數圖像系統不允許隱藏，BarBar 會在設定裡把它們標出來。

## 回報

這個儲存庫就是做這個的。遇到問題、想要什麼功能，都開
[Issue](https://github.com/imbbbbb/BarBar-support/issues/new/choose)。

回報 bug 時麻煩帶上 macOS 版本、BarBar 版本，以及是哪個 App 的圖像出的問題。

## 支持開發

BarBar 目前免費，但不承諾將來一直免費。如果它幫你把選單列收拾清爽了，
可以請我喝杯咖啡。

<a href="https://ko-fi.com/P4W31ZZFU0">
  <img src="https://img.shields.io/badge/%E5%9C%A8%20Ko--fi%20%E4%B8%8A%E6%94%AF%E6%8C%81%E6%88%91-72a4f2?style=for-the-badge&logo=ko-fi&logoColor=white" alt="在 Ko-fi 上支持我" height="38">
</a>

不支持也完全沒關係，提個 Issue 說說哪裡不好用，一樣有價值。

## 關於原始碼

BarBar 是閉源軟體，這個儲存庫只負責發佈和收集回饋，不包含原始碼。

它從零寫起，沒有沿用任何現成專案的程式碼。
