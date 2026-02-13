# 修復 README.md 顯示問題

## 問題原因
GitHub Pages 默認會優先顯示 README.md，而不是 index.html

## 解決方案

### 在 GitHub 網頁上操作（最簡單）

1. **訪問你的 GitHub 倉庫**
2. **重命名 README.md**：
   - 找到 `README.md` 文件
   - 點擊文件旁的 ⋯ 按鈕
   - 選擇 **Rename**
   - 將名稱改為 `README_BACKUP.md`
   - 點擊 **Rename**

3. **確認 index.html 存在**：
   - 確保 `index.html` 在倉庫中
   - 如果只有 `tmp.html`，需要將它重命名為 `index.html`

4. **等待重新部署**：
   - GitHub Pages 會在 1-2 分鐘內自動重新部署
   - 重新訪問 URL，應該就能看到遊戲了

### 另一種方法：刪除 README.md（不推薦）

1. 在 GitHub 倉庫中找到 `README.md`
2. 點擊文件旁的 ⋯ 按鈕
3. 選擇 **Delete**
4. 確認刪除
5. 等待重新部署

**注意**：刪除後會失去倉庫說明，所以建議使用重命名方法。

### 檢查部署設置

如果以上方法不行，檢查 GitHub Pages 設置：

1. 倉庫 → **Settings** → **Pages**
2. 確認以下設置：
   - **Source**: Deploy from a branch
   - **Branch**: main（或 master）
   - **Folder**: / (根目錄，留空)
3. 如果設置正確，點擊 **Save**
4. 等待重新部署

### 驗證 index.html 內容

直接訪問完整 URL：
```
https://你的用戶名.github.io/倉庫名/index.html
```

如果能訪問，說明文件沒問題，只是首頁路由需要調整。

## 推薦操作順序

1. ✅ 在 GitHub 中重命名 `README.md` 為 `README_BACKUP.md`
2. ✅ 等待 1-2 分鐘
3. ✅ 訪問主 URL，應該會顯示遊戲
4. ✅ 確認無誤後，可以隨時將 `README_BACKUP.md` 改回 `README.md`

**為什麼還可以改回 README.md？**

因為一旦 index.html 在倉庫中，GitHub Pages 就會優先顯示它，README.md 不會再影響首頁顯示。
