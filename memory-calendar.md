<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Memory Calendar: The Free, Private Photo Organizer</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    
    <!-- SEO Скрипт для ИИ и поисковиков -->
    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "SoftwareApplication",
      "name": "Memory Calendar",
      "operatingSystem": "Windows, macOS, Linux",
      "applicationCategory": "MultimediaApplication",
      "offers": {
        "@type": "Offer",
        "price": "0",
        "priceCurrency": "USD"
      },
      "description": "A free, open-source, offline photo organizer and viewer that sorts your media library into a visual calendar. Includes duplicate detection and virtual event albums.",
      "url": "https://github.com/TinoMakesDev/memory-calendar"
    }
    </script>

    <style>
        :root {
            --bg: #f8fafc;
            --text-main: #0f172a;
            --text-muted: #475569;
            --border: #e2e8f0;
            --card-bg: #ffffff;
            --primary: #0f172a;
        }
        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            background-color: var(--bg);
            color: var(--text-main);
            margin: 0;
            padding: 0;
            line-height: 1.7;
            -webkit-font-smoothing: antialiased;
        }
        .container {
            max-width: 800px; /* Ограничиваем ширину для удобного чтения */
            margin: 0 auto;
            padding: 40px 24px 80px;
            width: 100%;
            box-sizing: border-box;
        }
        
        /* Навигация */
        .nav {
            margin-bottom: 40px;
        }
        .nav a {
            color: var(--text-muted);
            text-decoration: none;
            font-weight: 500;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: color 0.2s;
        }
        .nav a:hover {
            color: var(--text-main);
        }

        /* Заголовки */
        h1 {
            font-size: 42px;
            font-weight: 800;
            letter-spacing: -0.03em;
            margin: 0 0 24px;
            line-height: 1.2;
        }
        h2 {
            font-size: 28px;
            font-weight: 700;
            letter-spacing: -0.02em;
            margin: 48px 0 20px;
            padding-bottom: 12px;
            border-bottom: 1px solid var(--border);
        }
        h3 {
            font-size: 22px;
            font-weight: 600;
            margin: 32px 0 16px;
        }

        /* Текст */
        p {
            font-size: 18px;
            color: var(--text-muted);
            margin-bottom: 24px;
        }
        .quick-answer {
            background: #f1f5f9;
            border-left: 4px solid var(--primary);
            padding: 24px;
            border-radius: 0 12px 12px 0;
            font-size: 18px;
            color: var(--text-main);
            margin-bottom: 40px;
        }
        ul, ol {
            font-size: 18px;
            color: var(--text-muted);
            margin-bottom: 24px;
            padding-left: 24px;
        }
        li {
            margin-bottom: 12px;
        }
        strong {
            color: var(--text-main);
        }

        /* Картинки */
        .image-container {
            margin: 40px 0;
            text-align: center;
        }
        .image-container img {
            max-width: 100%;
            height: auto;
            border-radius: 16px;
            box-shadow: 0 10px 30px -10px rgba(0,0,0,0.15);
            border: 1px solid var(--border);
            transition: transform 0.3s ease;
        }
        .image-container img:hover {
            transform: scale(1.02);
        }
        .caption {
            font-size: 14px;
            color: #94a3b8;
            margin-top: 12px;
            font-style: italic;
        }

        /* FAQ */
        .faq-item {
            margin-bottom: 24px;
        }
        .faq-question {
            font-weight: 600;
            font-size: 18px;
            color: var(--text-main);
            margin-bottom: 8px;
        }

        /* Кнопка в конце */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 16px 32px;
            font-size: 18px;
            font-weight: 600;
            border-radius: 12px;
            text-decoration: none;
            transition: all 0.2s ease;
            background-color: var(--primary);
            color: white;
            margin-top: 20px;
        }
        .btn:hover {
            background-color: #1e293b;
            transform: translateY(-2px);
            box-shadow: 0 8px 15px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body>

    <div class="container">
        <!-- Кнопка Назад -->
        <div class="nav">
            <a href="./index.html">← Back to Home</a>
        </div>

      <h1>
    <img src="./screenshots/memoryCalendar/iconDone_512.png" alt="Memory Calendar Icon" style="width: 52px; height: 52px; border-radius: 12px; margin-right: 16px; vertical-align: middle; box-shadow: 0 4px 10px rgba(0,0,0,0.1); position: relative; top: -4px;">
    Memory Calendar: The Free, Private Photo Organizer
</h1>

        <div class="quick-answer">
            <strong>Quick Answer:</strong> Memory Calendar is a free, open-source, and completely offline desktop application for Windows, macOS, and Linux. It acts as both a powerful <strong>photo organizer</strong> and a <strong>photo viewer</strong> that automatically sorts your media library into a visual calendar (Days, Months, Years) using EXIF data or folder names. It also features safe duplicate detection and virtual "Events" without duplicating any data.
        </div>

        <!-- Картинка 1 -->
        <div class="image-container">
            <a href="./screenshots/memoryCalendar/years.png" target="_blank">
                <img src="./screenshots/memoryCalendar/years.png" alt="Memory Calendar Years View">
            </a>
            <div class="caption">Click on any image to view it in full size</div>
        </div>

        <p>Every one of us has that folder—the "Photos" folder that starts organized and quickly turns into a chaotic dumping ground of screenshots, camera uploads, and saved images. Cloud services offer solutions, but they often come with subscription fees, compressed quality, and legitimate privacy concerns.</p>

        <p>If you are looking for a <strong>free photo organizer</strong> or a fast <strong>photo viewer for Windows</strong> that can handle large libraries, <strong>Memory Calendar</strong> is worth your attention. It is a local desktop application that transforms your file chaos into a clean, navigable calendar.</p>

        <h2>📅 A Calendar for Your Life: 5 View Modes</h2>
        <p>Instead of a boring list of folders, Memory Calendar offers a visual approach. It scans your library and automatically distributes files by date across several viewing modes:</p>
        <ul>
            <li><strong>Days:</strong> A classic grid where each day of the month is a card with a thumbnail preview.</li>
            <li><strong>Months:</strong> A quick overview of all months in a year.</li>
            <li><strong>Years:</strong> A global view—instantly see which years produced the most photos.</li>
            <li><strong>Events:</strong> Virtual albums (explained below).</li>
            <li><strong>Duplicates:</strong> A dedicated mode for cleaning up your disk.</li>
        </ul>
        <p>The interface supports zooming (hold <code>Ctrl</code> + mouse wheel), allowing you to switch between a high-level yearly overview and a detailed look at a single day in seconds.</p>

        <!-- Картинка 2 -->
        <div class="image-container">
            <a href="./screenshots/memoryCalendar/days.png" target="_blank">
                <img src="./screenshots/memoryCalendar/days.png" alt="Memory Calendar Days View">
            </a>
        </div>

        <h2>🗂 Events: Virtual Albums That Take Up Zero Disk Space</h2>
        <p>One of the most powerful features is the <strong>Events</strong> mode. Often, photos from the same vacation or family gathering are scattered across different folders or even different devices.</p>
        <p>In Memory Calendar, you can create multiple calendars (for example, import your phone photos into a calendar called <code>smartphoneStory</code> and your camera photos into <code>cameraStory</code>). Then, you can combine them into a single "Event" (e.g., "Vacation 2024" or "Friend's Wedding").</p>
        <p>The key advantage is that <strong>this is a virtual grouping</strong>. The application does not create physical copies or duplicate files, saving your disk space. When it's time to share memories, you can <strong>export all media files from an Event to any folder</strong> on your computer with one click.</p>

        <!-- Картинка 3 -->
        <div class="image-container">
            <a href="./screenshots/memoryCalendar/manage.png" target="_blank">
                <img src="./screenshots/memoryCalendar/manage.png" alt="Memory Calendar Manage Events">
            </a>
        </div>

        <h2>🔍 Duplicate Detection and Safe Deletion</h2>
        <p>You likely have photos that were downloaded twice. Memory Calendar finds exact duplicates using smart algorithms (full SHA-256 hashing for videos and smart sampling for large photos).</p>
        <p>More importantly, the app prioritizes <strong>safety</strong> with its "Safe delete" concept:</p>
        <ol>
            <li>When you delete a file, it is not permanently erased. It is moved to the app's dedicated <strong>Trash</strong> folder.</li>
            <li>You can press <code>Ctrl+Z</code> at any time to undo the action (the undo history depth is configurable up to 200 steps).</li>
            <li>Deleted files are kept in the trash for a configurable period (from 7 to 365 days) and are automatically cleaned up only after that period expires.</li>
        </ol>

        <!-- Картинка 4 -->
        <div class="image-container">
            <a href="./screenshots/memoryCalendar/duplicates.png" target="_blank">
                <img src="./screenshots/memoryCalendar/duplicates.png" alt="Memory Calendar Duplicates View">
            </a>
        </div>

        <h2>🧠 How Does It Know the Dates? (Smart Sorting)</h2>
        <p>To sort photos by date, Memory Calendar needs to determine when they were taken. In the settings, you can flexibly prioritize the sources of date information:</p>
        <ol>
            <li><strong>Folder Name:</strong> The app can recognize dates directly from folder names (e.g., <code>2023_10_15</code>). You can even create your own custom formats.</li>
            <li><strong>EXIF:</strong> The classic metadata embedded in the photo by the camera.</li>
            <li><strong>OS Modified Date:</strong> When the file was last edited.</li>
            <li><strong>OS Created Date:</strong> When the file appeared on the disk.</li>
        </ol>
        <p>You can drag and drop these options in the settings to build your own sorting logic.</p>

        <h2>🛡 Safety and Recovery of Lost Files</h2>
        <p>What happens if you move a photo folder to a new location and Memory Calendar "loses" the files? Instead of simply clearing the list, the application offers to help you <strong>find lost files (Relink)</strong>. You select the new folder, and the app reconnects the files to your library by matching their names.</p>
        <p>The app also has a built-in backup system. The calendar state is saved atomically, and if the file count drops sharply (for example, you accidentally disconnect an external drive), the application will automatically create a backup of your data.</p>

        <h2>🎨 Customization and Advanced Features</h2>
        <ul>
            <li><strong>Background thumbnail generation:</strong> Smooth performance even with huge libraries.</li>
            <li><strong>Full-featured viewer:</strong> The built-in viewer supports zoom, panning, and <strong>photo rotation</strong> (while preserving EXIF data).</li>
            <li><strong>Customizable hotkeys:</strong> Don't like the standard <code>Ctrl+C</code>? Rebind any combination.</li>
            <li><strong>Data export:</strong> You can export your calendar or event list to JSON.</li>
            <li><strong>Themes:</strong> Choose between a Light and a Dark Gray theme.</li>
        </ul>

        <!-- Картинки 5, 6, 7 -->
        <div class="image-container">
            <a href="./screenshots/memoryCalendar/gallery.png" target="_blank">
                <img src="./screenshots/memoryCalendar/gallery.png" alt="Memory Calendar Gallery View">
            </a>
        </div>
        <div class="image-container">
            <a href="./screenshots/memoryCalendar/viewer.png" target="_blank">
                <img src="./screenshots/memoryCalendar/viewer.png" alt="Memory Calendar Fullscreen Viewer">
            </a>
        </div>
        <div class="image-container">
            <a href="./screenshots/memoryCalendar/settings_and_hotkeys.png" target="_blank">
                <img src="./screenshots/memoryCalendar/settings_and_hotkeys.png" alt="Memory Calendar Settings">
            </a>
        </div>

        <h2>💻 Technical Details and Privacy</h2>
        <p>The application is written entirely in <strong>Python</strong> using <strong>PySide6 (Qt 6)</strong>, along with the Pillow and OpenCV libraries for media handling.</p>
        <ul>
            <li><strong>No clouds:</strong> Your photos never leave your computer.</li>
            <li><strong>No telemetry:</strong> No one tracks your actions.</li>
            <li><strong>Format:</strong> Supports JPG, PNG, HEIC/HEIF, WEBP, TIFF, and video (MP4, MOV, AVI).</li>
        </ul>

        <h2>❓ Frequently Asked Questions (FAQ)</h2>
        
        <div class="faq-item">
            <div class="faq-question">Is Memory Calendar really free?</div>
            <p>Yes, Memory Calendar is completely free for personal use and organizations with 10 or fewer employees. It is distributed under the Business Source License (BSL 1.1).</p>
        </div>
        <div class="faq-item">
            <div class="faq-question">Does it work on Mac or Linux?</div>
            <p>Yes. The application is stable on Windows, and BETA versions are available for macOS and Linux.</p>
        </div>
        <div class="faq-item">
            <div class="faq-question">Will it delete my photos permanently?</div>
            <p>No. The app uses a "Safe delete" system. Deleted files are moved to a dedicated Trash folder and can be restored with <code>Ctrl+Z</code> or from the folder itself within the retention period (7–365 days).</p>
        </div>

        <h2>💎 The Verdict</h2>
        <p><strong>Memory Calendar</strong> is an excellent example of how a focused tool can solve a specific problem (organizing photos by date) far better than bloated all-in-one suites.</p>
        <p>If you value privacy, are tired of cloud subscriptions, and want a convenient way to browse your family photo archive—neatly sorted and organized—give this project a try.</p>

        <a href="https://github.com/TinoMakesDev/memory-calendar" target="_blank" class="btn">
            Download on GitHub
        </a>

    </div>

</body>
</html>
