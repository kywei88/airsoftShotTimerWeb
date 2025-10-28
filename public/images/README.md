# 圖片使用指南

## 📁 目錄結構

```
static/images/
├── posts/      # 文章相關圖片
├── about/      # 關於頁面圖片
└── logos/      # Logo 和品牌圖片
```

## 📸 如何放置圖片

### 1. 將圖片複製到對應目錄

例如，將 Glock 17 的圖片放到：
```
static/images/posts/glock17.jpg
```

### 2. 在文章中引用圖片

**Markdown 語法：**
```markdown
![圖片描述](/images/posts/glock17.jpg)
```

**HTML 語法（更多控制）：**
```html
<img src="/images/posts/glock17.jpg" alt="Glock 17" width="600">
```

## 🎨 圖片尺寸建議

- **文章主圖（封面）**：1200 x 630 px
- **文章內圖片**：800 x 600 px 或更大
- **Logo**：透明背景 PNG，500 x 500 px

## 💡 範例

### 在 Glock 17 文章中使用圖片

```markdown
## Glock 17 生存遊戲訓練完全指南

![Glock 17 手槍](/images/posts/glock17.jpg)

Glock 17 是生存遊戲中最受歡迎的手槍之一...

### 1. 拔槍訓練

![拔槍訓練示範](/images/posts/draw-practice.jpg)

使用 AirsoftShotTimer 訓練從槍套快速拔槍...
```

## 🔗 支援的圖片格式

- JPG/JPEG（適合照片）
- PNG（適合透明背景、截圖）
- WebP（現代格式，檔案較小）
- SVG（向量圖形，適合 Logo）
- GIF（動態圖片）

## 📌 注意事項

1. **路徑必須以 `/` 開頭**：`/images/xxx.jpg`（不是 `images/xxx.jpg`）
2. **檔名建議使用英文**：避免中文檔名，使用 `-` 連接單字
3. **優化圖片大小**：壓縮圖片以加快載入速度
4. **添加 alt 文字**：有助於 SEO 和無障礙訪問
