# software-hw1

## 專案簡介

本專案為軟體課程第一次作業，基於 **Vue 3** 與 **Vite** 建立的前端部落格文章列表頁面。頁面包含左側分類導覽列與右側文章卡片列表，並實作了分類切換的互動功能，使用 Bootstrap 進行排版。

## 功能特色

- 🗂 **分類導覽**：左側可點擊的分類選單（品牌設計、平面設計、UIUX 設計、網頁設計、前端技術等），支援 Active 狀態切換。
- 📰 **文章列表**：每篇文章顯示封面圖片、分類標籤、標題、發布日期、觀看數與分享數。
- ⚡ **熱更新開發**：`npm run dev` 即時反映程式碼修改，大幅加速開發效率。
- 🔍 **ESLint / Oxlint 檢查**：整合 ESLint 與 Oxlint，確保程式碼品質一致。

## 開發環境需求

| 工具 | 建議版本 |
|------|----------|
| Node.js | 20.x 或以上 |
| npm | 10.x 或以上 |
| IDE | VS Code + [Vue - Official](https://marketplace.visualstudio.com/items?itemName=Vue.volar)（請停用 Vetur）|
| 瀏覽器 | Chrome / Edge / Brave（搭配 Vue DevTools）|

## 安裝步驟

```bash
# 1. 複製專案（若已有請跳過此步驟）
git clone <repository-url>
cd software-hw1

# 2. 安裝相依套件
npm install
```

## 使用方式

### 啟動開發模式（含熱更新）

```bash
npm run dev
```

啟動後開啟瀏覽器前往 `http://localhost:5173` 即可查看頁面。

### 產出正式版本

```bash
npm run build
```

產出檔案位於 `dist/` 目錄，可直接部署至任何靜態網頁伺服器。

### 程式碼格式檢查

```bash
npm run lint
```

執行 ESLint 檢查，自動修復可修正的問題。

## 專案結構

```
software-hw1/
├─ public/              # 靜態資源（不經 Vite 處理）
├─ src/
│   ├─ assets/          # 圖片、CSS 等資源
│   ├─ App.vue          # 根元件（導覽列 + 文章列表）
│   └─ main.js          # 應用程式入口
├─ index.html           # HTML 模板
├─ vite.config.js       # Vite 設定檔
├─ eslint.config.js     # ESLint 設定
├─ .prettierrc.json     # Prettier 格式設定
└─ package.json         # 套件清單與腳本
```

## 推薦瀏覽器擴充功能

- **Chromium 系（Chrome、Edge、Brave 等）**
  - [Vue.js devtools](https://chromewebstore.google.com/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd)
- **Firefox**
  - [Vue.js devtools](https://addons.mozilla.org/en-US/firefox/addon/vue-js-devtools/)

## 貢獻方式

1. Fork 本專案。
2. 建立功能分支：`git checkout -b feature/your-feature`
3. 提交並推送：`git push origin feature/your-feature`
4. 發起 Pull Request，並清楚描述變更內容。

## 授權

本專案採用 [MIT License](./LICENSE)。
