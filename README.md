# 赫蹏 mini

赫蹏（hètí）是專為中文內容展示設計的排版樣式增強。它基於通行的中文排版規範而來，可以為網站的讀者帶來更好的文章閱讀體驗。 

請參見原 repo 的更多說明：[sivan/heti](https://github.com/sivan/heti)（[貢獻者](https://github.com/sivan/heti/graphs/contributors)）。

此 mini 版移除了大多數 CSS 規則，且對繁體中文標點擠壓做了調整，便於部落格網站使用。

## 使用方法

1. 在頁面 `<html>` 標籤加入語言屬性，例如 `lang="zh-Hant-TW"` 或 `lang="zh-Hans-CN"`：

```html
<html lang="zh-Hant-TW">
```

2. 在需要使用赫蹏排版的元素上加入 `heti` 類，例如：

```html
<article class="heti">
```

3. 在頁面 `<head>` 標籤加入以下內容：

```html
<link rel="stylesheet" href="//unpkg.com/heti-mini/dist/heti.min.css">
<script src="//unpkg.com/heti-mini/dist/heti.min.js"></script>
<script>
  document.addEventListener('DOMContentLoaded', () => {
    const heti = new Heti('.heti');
    heti.autoSpacing();
  });
</script>
```

若頁面為動態載入，則可在須排版內容完全載入後再執行 `heti.autoSpacing()`。
