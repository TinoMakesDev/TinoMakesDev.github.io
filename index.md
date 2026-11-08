---
layout: home
title: "Welcome to TinoMakesDev"
---

I build free, privacy-focused, and local-first desktop applications. No clouds, no telemetry, just tools that respect your data and keep your files on your local disk.

<!-- Это скрипт поиска -->
<script src="https://unpkg.com/simple-jekyll-search@latest/dest/simple-jekyll-search.min.js"></script>

<!-- Поле ввода и контейнер для результатов -->
<div style="margin: 30px 0; padding: 20px; background-color: #f8f9fa; border-radius: 8px;">
  <input type="text" id="search-input" placeholder="Search the site (e.g., memory)..." style="width: 100%; padding: 12px; font-size: 16px; border: 1px solid #ddd; border-radius: 6px;">
  <ul id="results-container" style="margin-top: 15px; list-style-type: none; padding-left: 0;"></ul>
</div>

<!-- Настройка поиска -->
<script>
  SimpleJekyllSearch({
    searchInput: document.getElementById('search-input'),
    resultsContainer: document.getElementById('results-container'),
    json: '/search.json',
    searchResultTemplate: '<li style="margin-bottom: 10px;"><a href="{url}" style="font-size: 18px; color: #159957; text-decoration: none; font-weight: bold;">{title}</a></li>',
    noResultsText: 'No results found',
    limit: 10,
    fuzzy: false
  })
</script>

---

## 🚀 My Applications

### 📸 Memory Calendar
*A free, open-source, offline photo organizer and viewer that sorts your media library into a visual calendar (Days, Months, Years). Includes duplicate detection and virtual event albums.*

👉 **[Read the full article & features](./memory-calendar.html)**
👉 **[Download on GitHub](https://github.com/TinoMakesDev/memory-calendar)**

---
*(More apps coming soon...)*
