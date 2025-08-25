![Auto Assign](https://github.com/32iterations/demo-repository/actions/workflows/auto-assign.yml/badge.svg)
![Proof HTML](https://github.com/32iterations/demo-repository/actions/workflows/proof-html.yml/badge.svg)

# 32iterations 團隊官網

這是一個為 2025 梅竹黑客松參賽隊伍 "32iterations" 所打造的官方介紹網站。此專案為一個單頁式網站 (Single Page Application)，旨在以現代化、具備高度互動性的設計，完整呈現團隊成員的實力、戰略構想與專案潛力。

### ✨ 主要功能

- **現代化視覺設計**：採用柔和的漸層背景與抽象線條動畫，營造出富有創造力與科技感的氛圍。
- **互動式團隊介紹**：以水平滾動故事線的方式呈現團隊成員，點擊卡片可流暢展開，提供沉浸式的瀏覽體驗。
- **AI 驅動的內容生成**：整合 Google Gemini API，提供兩大 AI 互動功能：
    - **AI 腦力激盪**：即時為團隊生成一句響亮的口號 (Slogan)。
    - **專案細節產生**：針對團隊的四大專案構想，動態生成更深入的技術闡述。
- **響應式佈局**：在桌面、平板與行動裝置上皆有最佳的瀏覽效果。
- **平滑滾動與動畫**：全站採用平滑滾動，並搭配優雅的區塊淡入動畫，提升使用者體驗。

### 🚀 技術棧

- **前端**：HTML5, CSS3, JavaScript (ES6+)
- **CSS 框架**：[Tailwind CSS](https://tailwindcss.com/)
- **AI 模型**：[Google Gemini API](https://ai.google.dev/)

### 🏃 如何運行

這是一個純前端的專案，不需任何後端或複雜的建置步驟。

1.  直接在網頁瀏覽器中開啟 `index.html` 檔案即可預覽網站。
2.  若要使用 AI 相關功能，您需要在 JavaScript 程式碼中的 `apiKey` 變數填入您自己的 Google Gemini API 金鑰。

### 💡 程式碼結構亮點

專案的所有程式碼都包含在單一的 `index.html` 檔案中，方便快速部署與展示。

- **`<style>` 區塊**：定義了網站的核心視覺風格，包括主題色彩、漸層背景、動畫效果以及互動式團隊卡片的樣式。
- **`<script>` 區塊**：
    - **DOM 操作**：在 `DOMContentLoaded` 事件觸發後，動態生成團隊成員卡片，保持 HTML 結構的乾淨。
    - **互動邏輯**：包含了導覽列滾動、區塊淡入動畫，以及團隊卡片點擊展開的完整邏輯。
    - **Gemini API 整合**：
        - `prompts` 物件：預先定義了所有呼叫 AI 模型時所需的提示詞 (Prompt)，分類清晰，易於管理。這是與 Gemini 溝通的核心。
        - `callGeminiAPI` 函式：一個非同步 (async/await) 函式，封裝了所有與 Gemini API 互動的細節，包括發送請求、處理載入狀態、解析回傳結果以及錯誤處理。
