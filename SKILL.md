---
name: ai-science-inquiry-writer
description: Research and write source-backed Traditional Chinese articles that connect AI literacy with science inquiry, classroom practice, science fairs, biodiversity, environmental education, or hands-on experiments. Use when the user asks for an AI-and-science inquiry article, teaching feature, educator-facing technical article, inquiry case study, or a 2,000–3,000-character publishable article involving AI-assisted observation, identification, data analysis, verification, experimentation, or ecological investigation. For every completed article, always export downloadable UTF-8 plain-text and standalone HTML files with matching topic-related English filenames, expose the exact plain text in a Codex-copyable `text` code block, deploy the HTML to the prayer168/docs GitHub Pages site, and return the verified public URL.
---

# AI 與科學探究文章生成

將 AI 定位為觀察、整理、分析與提出候選解釋的助手，讓學生負責現場觀察、查證、推理與科學結論。預設使用臺灣繁體中文與臺灣教育語境。

## 執行流程

### 1. 確認寫作任務

從使用者提供的內容擷取：

- 主題、對象、篇幅、語氣與輸出格式。
- 科學概念、AI 用途、探究流程與延伸情境。
- 是否需要最新資料、引用、教材附件或 DOCX/PDF 等附加成品。純文字與 HTML 為每次固定輸出，不必另行詢問。

若使用者已提供足夠規格，直接執行，不重複提問。未指定時，預設撰寫 2,000–3,000 個中文字、適合國小高年級至國中教師閱讀的公開文章。

### 2. 建構探究核心

先形成一句核心主張，通常採用：

> AI 提供候選答案或資料整理，學生以觀察、查證、比較與解釋形成科學結論。

把主題轉換成可探究的事件鏈：

1. 觀察真實現象。
2. 提出可研究的問題。
3. 將 AI 輸出視為假設或候選解釋。
4. 蒐集現場資料與可信資料。
5. 比較證據並辨識矛盾。
6. 分析 AI 錯誤、偏差或不確定性。
7. 修正判斷並提出暫時性結論。
8. 指出限制與下一步研究。

依主題調整流程，不強行套用所有步驟。

### 3. 搜尋與查證

只要文章涉及最新技術、工具、政策、研究結果、資料庫或具體數據，就先搜尋。優先順序：

1. 臺灣教育部、農業部、環境部及其所屬機關。
2. 官方資料庫、課程綱要、博物館、植物園、大學與研究機構。
3. 同行評審論文、研究計畫或國際組織文件。
4. 工具官方文件；新聞或部落格僅作補充。

使用 5–10 筆與文章直接相關的來源。確認標題、發布單位、日期與連結可對應實際內容。找不到使用者指定的資料庫或機構名稱時，明確改用可驗證的替代來源，不虛構名稱或網址。

詳細查證與引用規格見 [references/editorial-standard.md](references/editorial-standard.md)。

### 4. 撰寫文章

以具體校園、實驗或戶外觀察場景開頭，讓讀者先看見問題。正文依下列邏輯自然推進：

- 現象與衝突：AI 快速回答，但答案可能不一致或缺乏證據。
- 探究過程：說明學生實際觀察、記錄、測量、查證與比較什麼。
- 科學概念：解釋分類、變因、證據、模型、相關與因果等必要概念。
- AI 素養：說明幻覺、資料偏差、辨識限制、信心與不確定性。
- 教師引導：用提問推動證據思考，不急著公布答案。
- 延伸研究：連結校園生態、昆蟲旅館、生物多樣性、科展或長期資料。
- 收束：回到「AI 提供可能性，學生用證據形成結論」。

使用有意義的小標題與完整段落。避免把正文寫成教案清單；必要的紀錄架構、比較欄位或操作步驟可使用短表格或精簡條列。

### 5. 區分人與 AI 的責任

清楚寫出：

- AI 可協助整理資料、產生候選辨識、繪製圖表、發現可能趨勢、提醒缺漏與提出後續問題。
- 學生負責現場觀察、拍照或測量、資料品質、來源查證、判斷合理性、解釋原因、指出限制與決定下一步。

不得暗示 AI 能直接證明因果、取代物種鑑定專家、代替實驗、或為科學結論負責。

### 6. 完成品質檢查

交稿前逐項確認：

- 全文符合指定篇幅、讀者與臺灣繁體中文。
- 有明確科學問題、證據來源與推理過程。
- 清楚區分現場觀察、AI 推測、資料庫記載與學生解釋。
- AI 錯誤被轉化為探究問題，而非只被描述成工具缺陷。
- 不把「同時發生」或統計相關寫成因果關係。
- 不虛構研究、工具功能、資料庫、政策、數據或網址。
- 所有具體事實與來源彼此對應；連結置於相關敘述附近或文末來源表。
- 結尾具啟發性但不喊口號、不說教。

### 7. 產生與驗證兩個檔案

每次完成文章後，固定在使用者指定的目錄產生下列兩個檔案；未指定時使用目前工作目錄：

1. `{english-topic-slug}.txt`：UTF-8 純文字，包含標題、正文與完整資料來源。保留清楚段落與完整網址，不含 Markdown 符號、HTML 標籤、寫作過程或操作說明。
2. `{english-topic-slug}.html`：UTF-8 單檔網頁，內容與純文字版一致，加入語意化標題、段落、清單、表格與可點擊來源。

根據文章主題翻譯並濃縮成 3–8 個有意義的英文關鍵字，建立小寫 ASCII kebab-case 主檔名。只使用 `a-z`、`0-9` 與連字號，不使用中文、空格、底線、無意義羅馬拼音或 Windows 禁用字元。例如「自然數位互動教材在教學上的應用」使用 `interactive-science-teaching-materials`。兩個檔案必須使用相同英文主檔名。

若同名檔案已存在且不是本次任務產物，在英文主檔名後加入 `-YYYYMMDD-HHmmss`，避免覆寫使用者檔案。建立檔案後確認實際檔名符合 `^[a-z0-9]+(?:-[a-z0-9]+)*\.(txt|html)$`。

HTML 必須：

- 使用 `lang="zh-Hant"`、`charset="utf-8"` 與 viewport 設定。
- 將所需 CSS 與 JavaScript 內嵌，不依賴外部 CDN，離線開啟仍可閱讀。
- 採 RWD 閱讀版面、清楚色彩對比、合理行距與最大欄寬。
- 開啟網頁後直接顯示文章，不得在頁面頂端、正文前或頁面其他位置加入「複製純文字」、「列印文章」或其他操作工具列與按鈕。
- 可提供適合瀏覽器原生列印的列印樣式，但不得另外顯示列印按鈕。
- 讓外部來源連結可點擊，並使用安全的開新頁設定。

交付前檢查兩個檔案皆存在、可用 UTF-8 讀取、標題與來源完整一致；檢查 HTML 結構、確認沒有操作工具列或按鈕、來源連結與窄螢幕排版。

### 8. 部署 HTML 到 GitHub Pages

兩個檔案驗證完成後，使用 `github-pages-html-deploy` 技能將本次產生的 `.html` 直接部署到下列固定站點；只部署 HTML，不把 `.txt` 加入 Pages 儲存庫：

- GitHub 儲存庫：`prayer168/docs`
- Pages 來源：`main` 分支根目錄
- 公開網址：`https://prayer168.github.io/docs/{english-topic-slug}.html`

部署時：

1. 先確認 GitHub CLI 已登入、儲存庫存在，而且 Pages 狀態與來源設定正確。
2. 若目前輸出目錄正是 `prayer168/docs` 的工作樹，直接在該工作樹操作；否則使用乾淨的暫存 checkout，避免把其他專案檔案混入。
3. 將 HTML 放在儲存庫根目錄並保留原本的英文檔名。提交前先 fetch，確認遠端進度與工作樹狀態。
4. 只 stage 本次 HTML，不 stage 純文字檔或任何無關變更；檢查 HTML 的標題及基本結構後再 commit、push 到 `main`。
5. 輪詢 Pages 建置狀態，並實際請求公開網址。只有在 HTTP 200 且頁面包含預期標題或正文識別文字後，才算部署完成。
6. 若同一內容已經在遠端，無須製造空提交，但仍須重新驗證公開網址。
7. 若因登入、權限、分支保護、衝突或 Pages 建置失敗而無法完成，不得宣稱已部署；保留本機成品並清楚回報阻礙。

最終回覆必須依序包含：

1. 簡短完成說明。
2. 標示為「GitHub Pages 網頁」的可點擊公開連結，並說明已完成線上驗證。
3. 標示為「下載純文字檔」與「下載網頁檔」的可點擊絕對路徑檔案連結，讓使用者可直接開啟或下載兩個本機成品。
4. 「一鍵複製純文字」標示。
5. 一個使用 `text` 或 `plaintext` 語言標記的 fenced code block，放入 `.txt` 的完整內容。Codex 會為此程式碼區塊提供一鍵複製按鈕。

程式碼區塊內只能放純文字檔內容，不得加入前言、檔名、註解或省略符號；不得截斷正文或資料來源。交付前逐字比較程式碼區塊與 `.txt`，確保兩者完全一致。即使文章較長，也不得以檔案連結取代此程式碼區塊。

## 輸出規格

每次固定交付使用相同主題英文檔名的 `.txt` 與 `.html`，提供可點擊下載連結，將 HTML 部署到 `https://prayer168.github.io/docs/` 並提供經驗證的公開網址，再於 Codex 最終回覆中以 `text` fenced code block 完整重現 `.txt`，讓使用者能使用內建按鈕一鍵複製。HTML 僅呈現文章內容，不加入複製、列印或其他操作工具列與按鈕。若使用者另要求 DOCX、PDF、簡報或學習單，再使用相應文件技能製作並驗證；這些附加格式不取代固定的兩個檔案、Pages 部署、下載連結與 Codex 一鍵複製區塊。

若主題可能涉及有毒植物、野外採集、過敏、動物干擾或其他安全風險，加入符合學生年齡的簡短安全提醒。
