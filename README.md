# 英雄旅程故事產生器

依照經典敘事結構,打造你的專屬英雄傳說。

## 設定說明

### 配置 GitHub Secrets

為了保護 API Key,請按照以下步驟設定 GitHub Secrets:

1. 前往你的 GitHub 儲存庫
2. 點擊 **Settings** (設定)
3. 在左側選單中找到 **Secrets and variables** > **Actions**
4. 點擊 **New repository secret**
5. 設定:
   - **Name**: `GROQ_API_KEY`
   - **Secret**: 貼上你的 Groq API Key (`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`)
6. 點擊 **Add secret**

### 啟用 GitHub Pages

1. 前往你的 GitHub 儲存庫
2. 點擊 **Settings** (設定)
3. 在左側選單中找到 **Pages**
4. 在 **Source** 下選擇 **GitHub Actions**
5. 儲存設定

### 部署

當你推送程式碼到 `main` 分支時,GitHub Actions 會自動:
1. 建置專案
2. 將 API Key 注入到 HTML 檔案中
3. 部署到 GitHub Pages

## 本地開發

如果要在本地測試,請將 `index.html` 中的 `{{GROQ_API_KEY}}` 暫時替換為你的實際 API Key。

**注意**: 請勿將包含真實 API Key 的檔案提交到 Git!

## 安全提醒

- ✅ API Key 儲存在 GitHub Secrets 中
- ✅ 只在部署時注入 API Key
- ✅ 原始碼中不包含真實的 API Key
- ⚠️ 前端應用仍會暴露 API Key 給使用者,建議未來考慮使用後端代理
