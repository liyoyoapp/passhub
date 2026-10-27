# PassHub — 智能會員卡與動態優惠聚合錢包

把散落在各個商場、超市、餐飲品牌的會員 App 收進同一個錢包：靜態條碼一鍵放大掃描，動態優惠一鍵跳轉。

## 功能

- **雙模卡片**
  - 靜態碼：上載／拍攝條碼或 QR Code，點擊進入大螢幕高亮度掃描模式（含 Wake Lock，避免掃描時熄屏）。
  - 動態連結：儲存網址，點擊直接開新視窗前往優惠頁。
- **搜尋與分類**：即時搜尋、類型分頁（全部／靜態碼／動態連結）、分類標籤（商場／超市／餐飲／交通／其他）。
- **新增／編輯／刪除**：表單驗證、拖放或選擇圖片、網址自動補 `https://`。
- **本地儲存**：資料存於瀏覽器 `localStorage`，重新整理不遺失；可一鍵重設示範資料。
- **行動優先 RWD**：手機雙欄卡片、底部彈出編輯器；桌面自動放大置中。

## 技術

- HTML5 + Tailwind CSS（CDN）
- FontAwesome 6.4（CDN）
- Vanilla JavaScript（ES6+）、LocalStorage API
- 無建置流程，單一 `index.html` 即可執行

## 本機使用

直接雙擊 `index.html`，或啟動簡易伺服器：

```bash
python3 -m http.server 5199
# 開啟 http://localhost:5199
```

> 首次開啟會載入示範資料（The Point、yuu、759、KFC、麥當勞、八達通）。

## 備註

- 網頁無法直接調整手機硬體亮度，「高亮度模式」以全白畫面 + Screen Wake Lock 實作。
- Tailwind 與 FontAwesome 使用 CDN，離線時樣式會失效；如需離線使用，可將 CSS 內嵌。
