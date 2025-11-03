# Hugo 專案結構與文章管理指南

## 專案資訊
- **專案名稱**: airsoftShotTimerWeb
- **框架**: Hugo
- **語言**: 繁體中文 (zh-tw) + 英文 (en)

## 文章存放位置

新的文章 md 檔案應放在：
```
content/posts/
```

## 文章命名規範

採用多語言設計，每篇文章需建立兩個版本：

- **繁體中文版**: `文章名稱.zh-tw.md`
- **英文版**: `文章名稱.en.md`

### 命名範例
```
content/posts/welcome.zh-tw.md
content/posts/welcome.en.md
content/posts/glock17-training-guide.zh-tw.md
content/posts/glock17-training-guide.en.md
```

## 建立新文章的方法

### 方法一：使用 Hugo CLI（推薦）

```bash
# 建立繁體中文文章
hugo new posts/文章slug.zh-tw.md

# 建立英文文章
hugo new posts/文章slug.en.md
```

### 方法二：手動建立

直接在 `content/posts/` 目錄中建立新的 `.md` 檔案。

## 目錄結構

```
.
├── archetypes/       # 文章模板
├── assets/           # 資源檔案
├── content/          # 內容目錄
│   ├── posts/       # 文章存放處 ⭐
│   ├── about.zh-tw.md
│   └── about.en.md
├── data/            # 資料檔案
├── layouts/         # 版面配置
├── static/          # 靜態檔案
├── themes/          # 主題
└── hugo.toml        # 設定檔
```

## 現有文章列表

1. `welcome.zh-tw.md` / `welcome.en.md`
2. `glock17-training-guide.zh-tw.md` / `glock17-training-guide.en.md`
3. `ipsc-training-guide.zh-tw.md` / `ipsc-training-guide.en.md`
4. `idpa-training-guide.zh-tw.md` / `idpa-training-guide.en.md`

## 文章模板

預設模板位於：`archetypes/default.md`

```toml
+++
date = '{{ .Date }}'
draft = true
title = '{{ replace .File.ContentBaseName "-" " " | title }}'
+++
```

## 注意事項

- 新建文章預設為 `draft = true`（草稿），發布前需改為 `false`
- 檔名使用小寫字母和連字號（kebab-case）
- 確保繁中和英文版本的檔名主體部分相同
