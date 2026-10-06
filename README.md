# index

**lsisan1212 專案入口** —— 一個 landing page，集中列出所有 GitHub Pages 與線上作品。

**線上位址**：https://lsisan1212.github.io/index/

## 結構

| 檔案 | 用途 |
|---|---|
| `index.html` | Landing page：卡片入口、搜尋、分類篩選、4 套主題 |
| `sites.json` | 專案清單 manifest（唯一要改嘅檔） |
| `.nojekyll` | 關 Jekyll |

## 現時收錄

| 分類 | 專案 | 網址 |
|---|---|---|
| 遊戲 | Games（Rummikub 拉密） | https://lsisan1212.github.io/Games/ |
| 量化 | Paper Trade Dashboard | https://lsisan1212.github.io/papertade/ |
| 工具 | BodyTrainer | https://lsisan1212.github.io/BodyTrainer/ |
| 工具 | MPA 我的專案傳送門 | https://lsisan1212.github.io/MPA/ |
| 工具 | HTML5 AI Player | https://lsisan1212.github.io/html-player/ |
| 工具 | Harness Bookmark Manager | https://lsisan1212.github.io/bookmark/ |
| 工具 | Markdown Notebook | https://lsisan1212.github.io/MDnote/ |
| 其他 | XBX 檔案目錄 | https://lsisan1212.github.io/xbx/ |
| 其他 | EdgeEver | https://edgeever.org |
| 其他 | Gemini Balance Lite | https://geminibalancelite-nine.vercel.app |

## 加新專案

1. 喺 `sites.json` 嘅 `sites` 陣列加一項：

```json
{
  "title": "新專案",
  "desc": "一句描述。",
  "url": "https://lsisan1212.github.io/NewThing/",
  "repo": "NewThing",
  "cat": "工具",
  "emoji": "🧰",
  "accent": "#5DCAA5",
  "tags": ["標籤"]
}
```

2. `git add -A && git commit -m "add: NewThing" && git push` → 約 30–60 秒生效

> 漏咗第 1 步都會自動顯示：頁面會經 GitHub API 讀 `lsisan1212` 嘅 public repo，未收錄嘅會以「自動偵測」分類補上（連去 repo 或 homepage）。

## 本地使用

```bash
open index.html
```

## 設計

- 單檔、零外部 CDN／框架／字型，`file://` 都跑得（有內建 fallback 清單）
- 4 套主題（深色／淺色／海洋／日落），`localStorage` 記住選擇
- 分類 chip + 搜尋（標題／描述／repo 名／標籤）
