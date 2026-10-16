# LINE 貼圖動畫編輯器

在手機上做 LINE 動態貼圖：疊圖層、設定動畫與關鍵格，直接匯出可上傳 LINE Creators Market 的 APNG。

**線上使用**：https://kftseng2oo1.github.io/Cmt/

## 主要功能
- 圖層：匯入圖片、Emoji、形狀、文字圖層，可拖曳位置、調整屬性
- 動畫：套用動畫效果、設定 FPS 與總長度、在時間軸加入關鍵格、循環播放預覽
- 匯出：靜態 PNG，或自行合成 APNG（不依賴外部函式庫）

## 使用方式
1. 「📁 匯入」貼圖素材，或用下方分頁新增文字、形狀
2. 選圖層設定動畫，必要時加「◆ 關鍵格」
3. ▶ 預覽，滿意後按「⬇ 匯出」→「開始匯出」

## 技術與依賴
- 單檔 HTML PWA（`index.html` 內含全部 HTML/CSS/JS），`manifest.json` + `sw.js` 提供安裝到主畫面與離線快取。
- Canvas 逐幀渲染，再手動組 PNG chunk（acTL/fcTL/fdAT）產生 APNG
- 全部在瀏覽器內處理，不上傳任何檔案

## 相關 repo
- [cut](https://github.com/kftseng2oo1/cut)：把整張貼圖表格裁成單張
