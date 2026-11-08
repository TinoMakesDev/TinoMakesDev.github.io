<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TinoMakesDev - Open Source Apps</title>
    <!-- Подключаем Tailwind CSS для современного дизайна -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body { font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; }
    </style>
</head>
<body class="bg-gray-50 text-gray-900 antialiased min-h-screen flex flex-col">

    <!-- Шапка -->
    <header class="bg-white border-b border-gray-200">
        <div class="max-w-4xl mx-auto px-6 py-8 text-center">
            <h1 class="text-4xl font-extrabold tracking-tight text-gray-900 mb-2">TinoMakesDev</h1>
            <p class="text-lg text-gray-500">Free, privacy-focused, and open-source desktop applications.</p>
        </div>
    </header>

    <!-- Основной контент -->
    <main class="flex-grow max-w-4xl mx-auto px-6 py-12 w-full">
        
        <!-- Рабочий поиск -->
        <div class="mb-12">
            <div class="relative max-w-xl mx-auto">
                <input type="text" id="searchInput" placeholder="Search applications (e.g., photo, calendar)..." 
                    class="w-full px-6 py-4 rounded-full border border-gray-300 shadow-sm focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent text-lg transition-all">
                <span class="absolute right-6 top-4 text-gray-400">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
                    </svg>
                </span>
            </div>
        </div>

        <!-- Сетка приложений -->
        <div class="grid gap-6 md:grid-cols-1" id="appGrid">
            
            <!-- Карточка приложения -->
            <div class="app-card bg-white rounded-2xl p-8 border border-gray-200 shadow-sm hover:shadow-md transition-shadow">
                <div class="flex items-center gap-4 mb-4">
                    <span class="text-4xl">📸</span>
                    <h2 class="text-2xl font-bold text-gray-900">Memory Calendar</h2>
                </div>
                <p class="text-gray-600 mb-6 text-lg leading-relaxed">
                    A free, open-source, offline photo organizer and viewer that sorts your media library into a visual calendar (Days, Months, Years). Includes duplicate detection and virtual event albums.
                </p>
                <div class="flex flex-wrap gap-4">
                    <a href="./memory-calendar.html" class="inline-flex items-center justify-center px-6 py-3 border border-transparent text-base font-medium rounded-lg text-white bg-blue-600 hover:bg-blue-700 transition-colors shadow-sm">
                        Read the full article
                    </a>
                    <a href="https://github.com/TinoMakesDev/memory-calendar" target="_blank" class="inline-flex items-center justify-center px-6 py-3 border border-gray-300 text-base font-medium rounded-lg text-gray-700 bg-white hover:bg-gray-50 transition-colors shadow-sm">
                        Download on GitHub
                    </a>
                </div>
            </div>

            <!-- Заглушка для будущих приложений -->
            <div class="text-center py-8 text-gray-400 italic">
                (More apps coming soon...)
            </div>

        </div>
    </main>

    <!-- Подвал -->
    <footer class="bg-white border-t border-gray-200 mt-auto">
        <div class="max-w-4xl mx-auto px-6 py-6 text-center text-gray-500 text-sm">
            &copy; 2026 TinoMakesDev.
        </div>
    </footer>

    <!-- Скрипт для рабочего поиска -->
    <script>
        document.getElementById('searchInput').addEventListener('input', function(e) {
            const searchTerm = e.target.value.toLowerCase();
            const cards = document.querySelectorAll('.app-card');
            
            cards.forEach(card => {
                const title = card.querySelector('h2').innerText.toLowerCase();
                const description = card.querySelector('p').innerText.toLowerCase();
                
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
