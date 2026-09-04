# AGENTS.md - 專案代理規範

## 專案資訊
- 名稱：capstone-course-design (Capstone 專題能力導向課程設計)
- 遠端：https://github.com/wuccjp/capstone-course-design
- 主分支：main

## 核心規則

### 1. 每次執行後必須 Commit
**任何一次任務、功能實作、Bug 修復、檔案變更完成後，必須立即執行 git commit（並 push）。**

流程：
```powershell
git status
git diff
git log --oneline -5
git add <變更檔案>  # 只加入本次任務相關檔案，不可濫用 git add .
git commit -m "type: 簡潔描述"
git push
```

禁止：
- 累積多次變更才一次 commit
- 產生檔案後不提交就結束任務
- 使用 --no-verify 跳過檢查

Commit 訊息規範：
- 格式：`type: 描述` (type: feat, fix, docs, refactor, chore, style)
- 使用中文或英文，簡潔明確
- 範例：`feat: 新增課程模組 API`、`fix: 修正評量計算錯誤`、`docs: 更新 AGENTS.md 提交規範`

### 2. 提交前檢查
- 執行 `git status` 確認變更範圍
- 執行相關測試/建置（若有）
- 確認不提交機敏資訊（.env, token, 密碼）

### 3. 語言與風格
- 回覆使用繁體中文，簡潔直接
- 引用程式碼時標註 `file_path:line_number`
- 優先驗證再總結，基於實際檔案內容回答

### 4. 檔案操作
- 優先編輯現有檔案而非新建
- 非必要不產生 *.md 文件
- 使用專用工具讀寫檔案（read/edit/write），bash 僅用於系統指令

## 驗證指令
```powershell
git status; git log --oneline -5; git remote -v
```
