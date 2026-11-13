# 織造用紗計算機

單一 HTML 檔案的用紗計算工具，不需安裝、不需後端，用手機或電腦瀏覽器直接開啟 `index.html` 即可使用。

<img src="icon-192.png" width="96" alt="icon">

## 計算公式

| 項目 | 公式 |
| --- | --- |
| ① 成品長度 | 盤頭長 × (1 − 織縮% ÷ 100) |
| ② 所需用紗量 | 成品數量 × 緯紗用紗量 (kg)；成品數量預設帶入成品長度，可手動修改 |
| ③ 剩餘未領量 | 領用紗量合計 − 所需用紗量 |
| ④ 已用紗量 | 已生產數量合計 × 緯紗用紗量 |
| ④ 廠內應餘紗 | 領用紗量合計 − 已用紗量 |
| ④ 比對差異 | 廠內庫存量合計 − 廠內應餘紗 |
| ④ 實際用紗量 | (領用量合計 − 庫存量合計) ÷ 已生產數量(碼)合計 |

領用紗量、已生產數量、廠內庫存量皆可多筆輸入，並提供複製與刪除鍵。

## 使用方式

- 直接雙擊 `index.html` 開啟。
- 或部署到 GitHub Pages（見下方）。

## 部署到 GitHub Pages

1. 在 GitHub 建立新的 repository（例如 `yarn-calculator`）。
2. 上傳本資料夾內所有檔案（`index.html`、`manifest.json`、`icon-192.png`、`icon-512.png`、`README.md`）。
3. 進入 **Settings → Pages**，Source 選擇 **Deploy from a branch**。
4. Branch 選 `main`，資料夾選 `/ (root)`，按 **Save**。
5. 等待約一分鐘，網址為 `https://<你的帳號>.github.io/yarn-calculator/`。

## 檔案說明

- `index.html`：計算機主程式（HTML、CSS、JavaScript 皆在同一檔案）
- `icon-192.png`、`icon-512.png`：網站與手機桌面圖示
- `manifest.json`：讓手機可「加入主畫面」，以 App 形式開啟
- `README.md`：說明文件
