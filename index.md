<html lang="en">
<head>
      <!-- Google tag (gtag.js) -->
    <script async src="https://www.googletagmanager.com/gtag/js?id=G-3D6N3Z0RWP"></script>
    <script>
      window.dataLayer = window.dataLayer || [];
      function gtag(){dataLayer.push(arguments);}
      gtag('js', new Date());

      gtag('config', 'G-3D6N3Z0RWP');
    </script>

    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TinoMakesDev - Source-Available Apps</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg: #f8fafc;
            --text-main: #0f172a;
            --text-muted: #64748b;
            --border: #e2e8f0;
            --card-bg: #ffffff;
            --btn-primary: #0f172a;
            --btn-hover: #1e293b;
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
            max-width: 760px;
            margin: 0 auto;
            padding: 0 24px;
            width: 100%;
            box-sizing: border-box;
        }
        header {
            padding: 80px 0 10px;
            text-align: center;
        }
        h1 {
            font-size: 48px;
            font-weight: 800;
            letter-spacing: -0.04em;
            margin: 0 0 16px;
            color: var(--text-main);
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
        
        /* Search */
        .search-container {
            margin: 40px auto 50px; 
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
            transition: all 0.3s ease;
            background-color: var(--card-bg);
            box-shadow: 0 1px 2px rgba(0,0,0,0.02);
            font-family: 'Inter', sans-serif;
        }
        .search-input:focus {
            border-color: #94a3b8;
            box-shadow: 0 4px 12px rgba(0,0,0,0.05);
        }
        .search-icon {
            position: absolute;
            left: 16px;
            top: 15px;
            color: #94a3b8;
            width: 20px;
            height: 20px;
        }

        /* App Cards */
        .app-card {
            background: var(--card-bg);
            border: 1px solid var(--border);
            border-radius: 20px;
            padding: 32px;
            margin-bottom: 24px;
            transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
            box-shadow: 0 1px 3px rgba(0,0,0,0.02);
            display: block;
            text-decoration: none;
            color: inherit;
            cursor: pointer;
        }
        .app-card:hover {
            transform: translateY(-6px);
            box-shadow: 0 20px 40px -10px rgba(0,0,0,0.08);
            border-color: #cbd5e1;
        }
        .app-header {
            display: flex;
            align-items: center;
            gap: 16px;
            margin-bottom: 16px;
        }
        
        .app-icon-img {
            width: 64px;
            height: 64px;
            border-radius: 16px;
            object-fit: cover;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
        }

        .app-title {
            font-size: 24px;
            font-weight: 700;
            margin: 0;
            letter-spacing: -0.02em;
        }
        .app-desc {
            color: var(--text-muted);
            font-size: 16px;
            line-height: 1.6;
            margin: 0 0 24px 0;
        }
        
        .app-actions {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
        }
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 14px 28px;
            font-size: 16px;
            font-weight: 600;
            border-radius: 12px;
            text-decoration: none;
            transition: all 0.2s ease;
            cursor: pointer;
            font-family: 'Inter', sans-serif;
        }
        .btn-primary {
            background-color: var(--btn-primary);
            color: white;
            border: 1px solid var(--btn-primary);
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        .btn-primary:hover {
            background-color: var(--btn-hover);
            transform: translateY(-2px);
            box-shadow: 0 8px 15px rgba(0,0,0,0.15);
        }
        .btn-secondary {
            background-color: transparent;
            color: var(--text-main);
            border: 1px solid var(--border);
        }
        .btn-secondary:hover {
            background-color: #f8fafc;
            border-color: #94a3b8;
        }

        footer {
            border-top: 1px solid var(--border);
            padding: 32px 0;
            text-align: center;
            color: #94a3b8;
            font-size: 14px;
        }
    </style>
</head>
<body>

    <header class="container">
        <h1>TinoMakesDev</h1>
        <p class="subtitle">Free, privacy-focused, and source-available applications.</p>
    </header>

    <main class="container">
        <div class="search-container">
            <svg class="search-icon" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
            </svg>
            <input type="text" id="searchInput" class="search-input" placeholder="Search (e.g., photo, calendar)...">
        </div>

        <div id="appGrid">
            <div class="app-card" onclick="window.location.href='./memory-calendar.html';">
                <div class="app-header">
                    <img src="./screenshots/memoryCalendar/iconDone_512.png" alt="Memory Calendar Icon" class="app-icon-img">
                    <h2 class="app-title">Memory Calendar</h2>
                </div>
                <p class="app-desc">
                    A free, source-available, offline photo organizer and viewer that sorts your media library into a visual calendar (Days, Months, Years). Includes duplicate detection and virtual event albums.
                </p>
                <div class="app-actions">
                    <a href="https://github.com/TinoMakesDev/memory-calendar" target="_blank" class="btn btn-primary" onclick="event.stopPropagation();">
                        Download on GitHub
                    </a>
                    <a href="./memory-calendar.html" class="btn btn-secondary">
                        Read Article
                    </a>
                </div>
            </div>

            <div style="text-align: center; color: #94a3b8; padding: 20px 0; font-size: 15px;">
                (More apps coming soon...)
            </div>

        </div>
    </main>

    <footer>
        <div class="container">
            &copy; 2026 TinoMakesDev.
        </div>
    </footer>

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
