# 部署說明

這個資料夾就是一個完整的網站，整個上傳即可，不需要任何後端或資料庫。

## 檔案內容

| 檔案 | 用途 |
|---|---|
| `index.html` | 主頁面：全文、圖表、參考文獻、補充資料、重點摘要、中文摘要、常見問題、引用格式 |
| `Wu2026_resilience_preprint.pdf` | 供下載的 PDF |
| `figures/` | 16 張圖（Fig. 1–5、Fig. S1–S11） |
| `paper.md` | 全文純文字版（Markdown），方便 AI 工具直接讀取 |
| `robots.txt` | 允許所有爬蟲（只有放在網站根目錄時才有作用） |

## 方法一：交給系所或實驗室網站

把整個資料夾交給網站管理員，請他放在一個固定網址下，例如
`https://www.econ.ntu.edu.tw/.../resilience-2026/`。
請確認：
- 頁面不需要登入就能看到
- 沒有被設定成禁止搜尋引擎收錄（noindex）

## 方法二：GitHub Pages（免費）

1. 登入 GitHub，建立一個新的公開 repository，例如 `resilience-2026`。
2. 點「uploading an existing file」，把這個資料夾裡的所有檔案（含 `figures` 資料夾）拖進去，按 Commit。
3. 到 Settings → Pages，Source 選「Deploy from a branch」，Branch 選 `main`、資料夾選 `/ (root)`，存檔。
4. 約 1–2 分鐘後，網址會是 `https://你的帳號.github.io/resilience-2026/`。

## 上線後要做的事

1. 打開網址，確認全文、圖片和 PDF 下載都正常。
2. 到 Google Search Console 加入網站並提交網址，加快 Google 收錄。
3. 把網址加到：ORCID 個人頁（Websites）、Google Scholar 個人頁、Bluesky 個人簡介、實驗室網頁。
4. 在 bioRxiv 上傳新版本時，記得同步更新這個網頁。

## 選做：填入正式網址

上線後如果知道正式網址，可以在 `index.html` 的 `<head>` 裡加一行（把網址換成實際的）：

```html
<link rel="canonical" href="https://你的網址/">
```

## 授權

全文與圖表依 bioRxiv 上相同的 CC BY-NC-ND 4.0 授權公開。公開前請先取得所有共同作者同意。
頁面上的「Key findings」「中文摘要」「Questions this study answers」三段是根據論文內容整理的摘要，上線前請作者確認內容正確。
