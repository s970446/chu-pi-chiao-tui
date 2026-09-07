# 硃筆校對 Chu-pi Chiao-tui

PDF 引文標點與斷行校正小工具。純前端、無後端、無 API，所有處理都在瀏覽器本機完成，文字內容不會離開使用者的電腦。


## 功能

- 半形標點轉全形（，。：；！？（）），並排除數字千分位（`199,885`）與小數點（`3.14`）的誤判
- 合併 PDF 複製貼上造成的排版斷行，並清理多餘空格，以空白行 / 行首縮排判斷段落分界
- 簡體轉繁體（字元對照轉換，可選開關）
- 可自訂「尋找／取代」規則，支援一般文字或正則表達式
- 校正後文字欄位可直接手動編輯

## 部署到 GitHub Pages

1. 在 GitHub 建立一個新的 public 儲存庫（例如命名為 `chu-pi-chiao-tui`）
2. 把這個資料夾裡的 `index.html` 上傳到儲存庫的根目錄（或 `/docs` 資料夾，兩者擇一即可）
3. 到儲存庫的 **Settings → Pages**
4. 在 **Build and deployment** 底下的 **Source** 選擇 **Deploy from a branch**
5. **Branch** 選擇 `main`，資料夾選擇 `/ (root)`（如果第 2 步放在 `/docs`，這裡就選 `/docs`）
6. 儲存後等待約 1 分鐘，頁面就會出現在：
   `https://<你的 GitHub 帳號>.github.io/chu-pi-chiao-tui/`

> 小提醒：如果之後在同一個儲存庫放其他 Markdown 檔案，GitHub Pages 預設會用 Jekyll 處理，通常不影響純 HTML 頁面正常顯示；如果遇到顯示異常，可以在根目錄加一個空白檔案 `.nojekyll` 來停用 Jekyll 處理。

## 致謝與授權

- 簡體轉繁體的字元對照表取自 [OpenCC](https://github.com/BYVoid/OpenCC) 專案的 `STCharacters.txt` 與 `TWVariants.txt`，採 Apache-2.0 授權。若公開發布本工具，建議保留 `index.html` 原始碼中對應的授權註解。
- 字型使用 Google Fonts 的 Noto Serif TC / Noto Sans TC，透過 `<link>` 標籤載入。
- 本工具其餘程式碼（HTML／CSS／JavaScript）目前未附加授權條款；如果你想以開源方式釋出，可以自行加上一個 `LICENSE` 檔案（例如 MIT），或保留為僅供個人使用。
