---
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TinoMakesDev - Open Source Apps</title>
    <!-- Подключаем современный шрифт Inter -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg: #fafafa;
            --text-main: #111111;
            --text-muted: #666666;
            --primary: #000000; /* Строгий черный, как у Apple */
            --border: #eaeaea;
            --card-bg: #ffffff;
        }
        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            background-color: var(--bg);
            color: var(--text-main);
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
            -webkit-font-smoothing: antialiased;
        }
        .container {
            max-width: 720px;
            margin: 0 auto;
            padding: 0 24px;
            width: 100%;
            box-sizing: border-box;
        }
        header {
            padding: 80px 0 50px;
            text-align: center;
        }
        h1 {
            font-size: 48px;
            font-weight: 800;
            letter-spacing: -0.04em;
            margin: 0 0 16px;
        }
        .subtitle {
            font-size: 20px;
            color: var(--text-muted);
            margin: 0;
            font-weight: 400;
        }
        main {
            flex-grow: 1;
            padding-bottom: 60px;
        }
        
        /* Поиск */
        .search-container {
            margin: 0 auto 40px;
            max-width: 480px;
            position: relative;
        }
        .search-input {
            width: 100%;
            padding: 14px 20px 14px 48px;
            font-size: 16px;
            border: 1px solid var(--border);
            border-radius: 12px;
            box-sizing: border-box;
            outline: none;
            transition: all 0.2s ease;
            background-color: var(--card-bg);
            box-shadow: 0 1px 2px rgba(0,0,0,0.02);
            font-family: 'Inter', sans-serif;
        }
        .search-input:focus {
            border-color: #999;
            box-shadow: 0 4px 12px rgba(0,0,0,0.05);
        }
        .search-icon {
            position: absolute;
            left: 16px;
            top: 15px;
            color: #999;
            width: 20px;
            height: 20px;
        }

        /* Карточки */
        .app-card {
            background: var(--card-bg);
            border: 1px solid var(--border);
            border-radius: 16px;
            padding: 32px;
            margin-bottom: 24px;
            transition: all 0.2s ease;
            box-shadow: 0 1px 3px rgba(0,0,0,0.02);
            display: block;
            text-decoration: none;
            color: inherit;
        }
        .app-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 12px 24px -8px rgba(0,0,0,0.08);
            border-color: #d0d0d0;
        }
        .app-header {
            display: flex;
            align-items: center;
            gap: 16px;
            margin-bottom: 16px;
        }
        .app-icon {
            font-size: 36px;
            background: #f5f5f5;
            padding: 12px;
            border-radius: 12px;
            line-height: 1;
        }
        .app-title {
            font-size: 24px;
            font-weight: 700;
            margin: 0;
            letter-spacing: -0.02em;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        /* Стрелочка, которая появляется при наведении на карточку */
        .app-title::after {
            content: "→";
            opacity: 0;
            transition: opacity 0.2s, transform 0.2s;
            transform: translateX(-5px);
            font-weight: 400;
        }
        .app-card:hover .app-title::after {
            opacity: 1;
            transform: translateX(0);
        }
        .app-desc {
            color: var(--text-muted);
            font-size: 16px;
            line-height: 1.6;
            margin: 0;
        }
        footer {
            border-top: 1px solid var(--border);
            padding: 32px 0;
            text-align: center;
            color: #999;
            font-size: 14px;
        }
    </style>
</head>
<body>

    <header class="container">
        <h1>TinoMakesDev</h1>
        <p class="subtitle">Free, privacy-focused, and open-source applications.</p>
    </header>

    <main class="container">
        <!-- Поиск -->
        <div class="search-container">
            <svg class="search-icon" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
            </svg>
            <input type="text" id="searchInput" class="search-input" placeholder="Search (e.g., photo, calendar)...">
        </div>

        <!-- Сетка приложений -->
        <div id="appGrid">
            
            <!-- Карточка (теперь полностью кликабельная) -->
            <a href="./memory-calendar.html" class="app-card">
                <div class="app-header">
                    <span class="app-icon">📸</span>
                    <h2 class="app-title">Memory Calendar</h2>
                </div>
                <p class="app-desc">
                    A free, open-source, offline photo organizer and viewer that sorts your media library into a visual calendar (Days, Months, Years). Includes duplicate detection and virtual event albums.
                </p>
            </a>

            <!-- Заглушка -->
            <div style="text-align: center; color: #999; padding: 20px 0; font-size: 15px;">
                (More apps coming soon...)
            </div>

        </div>
    </main>

    <footer>
        <div class="container">
            &copy; 2026 TinoMakesDev. All rights reserved.
        </div>
    </footer>

    <!-- Скрипт для рабочего поиска -->
    <script>
        document.getElementById('searchInput').addEventListener('input', function(e) {
            const searchTerm = e.target.value.toLowerCase();
            const cards = document.querySelectorAll('.app-card');
            
            cards.forEach(card => {
                const title = card.querySelector('.app-title').innerText.toLowerCase();
                const description = card.querySelector('.app-desc').innerText.toLowerCase();
                
                if (title.includes(searchTerm) || description.includes(searchTerm)) {
                    card.style.display = 'block';
                } else {
                    card.style.display = 'none';
                }
            });
        });
    </script>
</body>
</html>
