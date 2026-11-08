---
layout: null
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TinoMakesDev - Open Source Apps</title>
    <!-- Подключаем шрифт Inter -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-gradient: radial-gradient(circle at top, #ffffff 0%, #f3f4f6 100%);
            --text-main: #111827;
            --text-muted: #6b7280;
            --border: #e5e7eb;
            --card-bg: #ffffff;
            --accent: #000000;
        }
        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            background: var(--bg-gradient);
            color: var(--text-main);
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
            -webkit-font-smoothing: antialiased;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 0 24px;
            width: 100%;
            box-sizing: border-box;
        }
        header {
            padding: 100px 0 60px;
            text-align: center;
        }
        h1 {
            font-size: 52px;
            font-weight: 800;
            letter-spacing: -0.04em;
            margin: 0 0 16px;
            background: linear-gradient(135deg, #111 0%, #333 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .subtitle {
            font-size: 20px;
            color: var(--text-muted);
            margin: 0;
            font-weight: 400;
        }
        main {
            flex-grow: 1;
            padding-bottom: 80px;
        }
        
        /* Поиск */
        .search-container {
            margin: 0 auto 48px;
            max-width: 480px;
            position: relative;
        }
        .search-input {
            width: 100%;
            padding: 16px 24px 16px 52px;
            font-size: 16px;
            border: 1px solid var(--border);
            border-radius: 100px;
            box-sizing: border-box;
            outline: none;
            transition: all 0.3s ease;
            background-color: rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(10px);
            box-shadow: 0 4px 6px -1px rgba(0,0,0,0.02);
            font-family: 'Inter', sans-serif;
        }
        .search-input:focus {
            border-color: #9ca3af;
            box-shadow: 0 10px 25px -5px rgba(0,0,0,0.05);
            background-color: #fff;
        }
        .search-icon {
            position: absolute;
            left: 20px;
            top: 17px;
            color: #9ca3af;
            width: 20px;
            height: 20px;
        }

        /* Карточки */
        .app-card {
            background: var(--card-bg);
            border: 1px solid var(--border);
            border-radius: 24px; /* Более круглые углы */
            padding: 40px;
            margin-bottom: 24px;
            transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
            box-shadow: 0 1px 2px rgba(0,0,0,0.02);
            display: block;
            text-decoration: none;
            color: inherit;
            position: relative;
            overflow: hidden;
        }
        /* Эффект свечения при наведении */
        .app-card::before {
            content: "";
            position: absolute;
            top: 0; left: 0; right: 0; height: 100%;
            background: radial-gradient(800px circle at var(--mouse-x) var(--mouse-y), rgba(0,0,0,0.03), transparent 40%);
            opacity: 0;
            transition: opacity 0.4s;
            pointer-events: none;
        }
        .app-card:hover::before {
            opacity: 1;
        }
        .app-card:hover {
            transform: translateY(-4px) scale(1.01);
            box-shadow: 0 20px 40px -10px rgba(0,0,0,0.08);
            border-color: #d1d5db;
        }
        .app-header {
            display: flex;
            align-items: center;
            gap: 16px;
            margin-bottom: 16px;
        }
        .app-icon {
            font-size: 32px;
            background: #f3f4f6;
            width: 64px;
            height: 64px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 16px;
            box-shadow: inset 0 2px 4px rgba(255,255,255,0.5), 0 2px 4px rgba(0,0,0,0.05);
        }
        .app-title {
            font-size: 26px;
            font-weight: 700;
            margin: 0;
            letter-spacing: -0.02em;
            display: flex;
            align-items: center;
            gap: 12px;
        }
        .app-title::after {
            content: "→";
            opacity: 0;
            transition: opacity 0.2s, transform 0.3s;
            transform: translateX(-10px);
            font-weight: 400;
            color: #9ca3af;
        }
        .app-card:hover .app-title::after {
            opacity: 1;
            transform: translateX(0);
        }
        .app-desc {
            color: var(--text-muted);
            font-size: 17px;
            line-height: 1.6;
            margin: 0;
            max-width: 90%;
        }
        footer {
            border-top: 1px solid var(--border);
            padding: 32px 0;
            text-align: center;
            color: #9ca3af;
            font-size: 14px;
            background: rgba(255,255,255,0.5);
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

        <div id="appGrid">
            
            <!-- Карточка (полностью кликабельная) -->
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
            <div style="text-align: center; color: #9ca3af; padding: 20px 0; font-size: 15px;">
                (More apps coming soon...)
            </div>

        </div>
    </main>

    <footer>
        <div class="container">
            &copy; 2026 TinoMakesDev.
        </div>
    </footer>

    <!-- Поиск и эффект мыши на карточках -->
    <script>
        // Поиск
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

        // Эффект "фонарика" на карточке
        document.querySelectorAll('.app-card').forEach(card => {
            card.addEventListener('mousemove', e => {
                const rect = card.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                card.style.setProperty('--mouse-x', `${x}px`);
                card.style.setProperty('--mouse-y', `${y}px`);
            });
        });
    </script>
</body>
</html>
