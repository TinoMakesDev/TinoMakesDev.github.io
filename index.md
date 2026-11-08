---
layout: default
title: "Memory Calendar: The Free, Private Photo Organizer"
---

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

# 📸 Memory Calendar: The Free, Private Photo Organizer and Viewer

**Quick Answer:** Memory Calendar is a free, open-source, and completely offline desktop application for Windows, macOS, and Linux. It acts as both a powerful **photo organizer** and a **photo viewer** that automatically sorts your media library into a visual calendar (Days, Months, Years) using EXIF data or folder names. It also features safe duplicate detection and virtual "Events" without duplicating any data.

![Memory Calendar's Years view showing a grid of photos organized by year - free photo organizer](./years-view.png)

Every one of us has that folder—the "Photos" folder that starts organized and quickly turns into a chaotic dumping ground of screenshots, camera uploads, and saved images. Cloud services offer solutions, but they often come with subscription fees, compressed quality, and legitimate privacy concerns.

If you are looking for a **free photo organizer** or a fast **photo viewer for Windows** that can handle large libraries, **Memory Calendar** is worth your attention. It is a local desktop application that transforms your file chaos into a clean, navigable calendar. This article covers how it works, its hidden features, and why it might become your go-to photo management tool.

### 📅 A Calendar for Your Life: 5 View Modes

Instead of a boring list of folders, Memory Calendar offers a visual approach. It scans your library and automatically distributes files by date across several viewing modes:

- **Days:** A classic grid where each day of the month is a card with a thumbnail preview.
- **Months:** A quick overview of all months in a year.
- **Years:** A global view—instantly see which years produced the most photos.
- **Events:** Virtual albums (explained below).
- **Duplicates:** A dedicated mode for cleaning up your disk.

The interface supports zooming (hold `Ctrl` + mouse wheel), allowing you to switch between a high-level yearly overview and a detailed look at a single day in seconds.

![Memory Calendar's Days view showing photos sorted by date - image organizer software](./days-view.png)

### 🗂 Events: Virtual Albums That Take Up Zero Disk Space

One of the most powerful features is the **Events** mode. Often, photos from the same vacation or family gathering are scattered across different folders or even different devices.

In Memory Calendar, you can create multiple calendars (for example, import your phone photos into a calendar called `smartphoneStory` and your camera photos into `cameraStory`). Then, you can combine them into a single "Event" (e.g., "Vacation 2024" or "Friend's Wedding"). The key advantage is that **this is a virtual grouping**. The application does not create physical copies or duplicate files, saving your disk space. When it's time to share memories, you can **export all media files from an Event to any folder** on your computer with one click.

### 🔍 Duplicate Detection and Safe Deletion

You likely have photos that were downloaded twice. Memory Calendar finds exact duplicates using smart algorithms (full SHA-256 hashing for videos and smart sampling for large photos).

More importantly, the app prioritizes **safety** with its "Safe delete" concept:
1.  When you delete a file, it is not permanently erased. It is moved to the app's dedicated **Trash** folder.
2.  You can press `Ctrl+Z` at any time to undo the action (the undo history depth is configurable up to 200 steps).
3.  Deleted files are kept in the trash for a configurable period (from 7 to 365 days) and are automatically cleaned up only after that period expires.

### 🧠 How Does It Know the Dates? (Smart Sorting)

To sort photos by date, Memory Calendar needs to determine when they were taken. In the settings, you can flexibly prioritize the sources of date information:

1.  **Folder Name:** The app can recognize dates directly from folder names (e.g., `2023_10_15`). You can even create your own custom formats.
2.  **EXIF:** The classic metadata embedded in the photo by the camera.
3.  **OS Modified Date:** When the file was last edited.
4.  **OS Created Date:** When the file appeared on the disk.

You can drag and drop these options in the settings to build your own sorting logic.

### 🛡 Safety and Recovery of Lost Files

What happens if you move a photo folder to a new location and Memory Calendar "loses" the files? Instead of simply clearing the list, the application offers to help you **find lost files (Relink)**. You select the new folder, and the app reconnects the files to your library by matching their names.

The app also has a built-in backup system. The calendar state is saved atomically, and if the file count drops sharply (for example, you accidentally disconnect an external drive), the application will automatically create a backup of your data.

### 🎨 Customization and Advanced Features

Memory Calendar is not just about sorting; it is also about comfort:

- **Background thumbnail generation:** Smooth performance even with huge libraries. All thumbnails are cached in a separate folder (you can change the cache path and safely clear the cache).
- **Full-featured viewer:** The built-in viewer supports zoom, panning, and **photo rotation** (while preserving EXIF data).
- **Customizable hotkeys:** Don't like the standard `Ctrl+C`? Rebind any combination. There are even profiles for Windows, macOS, and Linux.
- **Data export:** You can export your calendar or event list to JSON (useful for backups or migration).
- **Themes:** Choose between a Light and a Dark Gray theme.
- **Localization:** If English doesn't suit you, you can export a template, translate it, and load your own language file.

![Memory Calendar Settings - customize hotkeys and cache](./settings.png)

### 💻 Technical Details and Privacy

The application is written entirely in **Python** using **PySide6 (Qt 6)**, along with the Pillow and OpenCV libraries for media handling.

This means:
- **No clouds:** Your photos never leave your computer.
- **No telemetry:** No one tracks your actions.
- **Format:** The entire project is distributed as a single `.py` file that is easy to run locally. It supports popular formats: JPG, PNG, HEIC/HEIF (via `pillow-heif`), WEBP, TIFF, as well as video (MP4, MOV, AVI).

### ❓ Frequently Asked Questions (FAQ)

**Is Memory Calendar really free?**
Yes, Memory Calendar is completely free for personal use and organizations with 10 or fewer employees. It is distributed under the Business Source License (BSL 1.1).

**Does it work on Mac or Linux?**
Yes. The application is stable on Windows, and BETA versions are available for macOS and Linux.

**Will it delete my photos permanently?**
No. The app uses a "Safe delete" system. Deleted files are moved to a dedicated Trash folder and can be restored with `Ctrl+Z` or from the folder itself within the retention period (7–365 days).

**Can I use it completely offline?**
Absolutely. Memory Calendar is designed with privacy in mind. It requires no internet connection, has no cloud sync, and collects zero telemetry.

### 💎 The Verdict

**Memory Calendar** is an excellent example of how a focused tool can solve a specific problem (organizing photos by date) far better than bloated all-in-one suites. 

If you value privacy, are tired of cloud subscriptions, and want a convenient way to browse your family photo archive—neatly sorted and organized—give this project a try.

👉 **Download the latest version and view the source code on GitHub:** [TinoMakesDev/memory-calendar](https://github.com/TinoMakesDev/memory-calendar)
