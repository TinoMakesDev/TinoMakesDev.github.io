<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TinoMakesDev - Open Source Apps</title>
    <style>
        :root {
            --bg: #f9fafb;
            --text-main: #111827;
            --text-muted: #6b7280;
            --primary: #2563eb;
            --primary-hover: #1d4ed8;
            --border: #e5e7eb;
            --card-bg: #ffffff;
        }
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
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
            max-width: 800px;
            margin: 0 auto;
            padding: 0 24px;
            width: 100%;
            box-sizing: border-box;
        }
        header {
            padding: 60px 0 40px;
            text-align: center;
        }
        h1 {
            font-size: 42px;
            font-weight: 800;
            letter-spacing: -0.02em;
            margin: 0 0 12px;
        }
        .subtitle {
            font-size: 20px;
            color: var(--text-muted);
            margin: 0;
        }
        main {
            flex-grow: 1;
            padding-bottom: 60px;
        }
        /* Поиск */
        .search-container {
            margin: 0 auto 48px;
            max-width: 500px;
            position: relative;
        }
        .search-input {
            width: 100%;
            padding: 16px 24px;
            font-size: 16px;
            border: 1px solid var(--border);
            border-radius: 50px;
            box-sizing: border-box;
            outline: none;
            transition: box-shadow 0.2s, border-color 0.2s;
            background-color: var(--card-bg);
        }
        .search-input:focus {
            border-color: var(--primary);
            box-shadow: 0 0 0 4px rgba(37, 99, 235, 0.1);
        }
        /* Карточки */
        .app-card {
            background: var(--card-bg);
            border: 1px solid var(--border);
            border-radius: 16px;
            padding: 32px;
            margin-bottom: 24px;
            transition: transform 0.2s, box-shadow 0.2s;
            box-shadow: 0 1px 3px rgba(0,0,0,0.05);
        }
        .app-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 15px -3px rgba(0,0,0,0.1);
        }
        .app-header {
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 16px;
        }
        .app-icon {
            font-size: 32px;
        }
        .app-title {
            font-size: 24px;
            font-weight: 700;
            margin: 0;
        }
        .app-title a {
            color: var(--text-main);
            text-decoration: none;
        }
        .app-title a:hover {
            color: var(--primary);
        }
        .app-desc {
            color: var(--text-muted);
            font-size: 17px;
            line-height: 1.6;
            margin: 0 0 24px;
        }
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 10px 20px;
            font-size: 15px;
            font-weight: 600;
            border-radius: 8px;
            text-decoration: none;
            transition: background-color 0.2s;
            border: 1px solid transparent;
        }
        .btn-primary {
            background-color: var(--text-main);
            color: white;
        }
        .btn-primary:hover {
            background-color: #374151;
        }
        .btn-outline {
            border-color: var(--border);
            color: var(--text-main);
            background-color: transparent;
        }
        .btn-outline:hover {
            background-color: var(--bg);
        }
        footer {
            border-top: 1px solid var(--border);
            padding: 24px 0;
            text-align: center;
            color: var(--text-muted);
            font-size: 14px;
        }
    </style>
</head>
<body>

    <header class="container">
        <h1>TinoMakesDev</h1>
        <p class="subtitle">Free, privacy-focused, and open-source desktop applications.</p>
    </header>

    <main class="container">
        <!-- Поиск -->
        <div class="search-container">
            <input type="text" id="searchInput" class="search-input" placeholder="Search applications (e.g., photo, calendar)...">
        </div>

        <!-- Сетка приложений -->
        <div id="appGrid">
            
            <!-- Карточка 1 -->
            <div class="app-card">
                <div class="app-header">
                    <span class="app-icon">📸</span>
                    <h2 class="app-title"><a href="./memory-calendar.html">Memory Calendar</a></h2>
                </div>
                <p class="app-desc">
                    A free, open-source, offline photo organizer and viewer that sorts your media library into a visual calendar (Days, Months, Years). Includes duplicate detection and virtual event albums.
                </p>
                <div style="display: flex; gap: 12px; flex-wrap: wrap;">
                    <a href="https://github.com/TinoMakesDev/memory-calendar" target="_blank" class="btn btn-primary">
                        Download on GitHub
                    </a>
                </div>
            </div>

            <!-- Заглушка -->
            <div style="text-align: center; color: var(--text-muted); padding: 40px 0; font-style: italic;">
                (More apps coming soon...)
            </div>

        </div>
    </main>

    <footer>
        <div class="container">
            &copy; 2026 TinoMakesDev.
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
