# Battery Health Report (iOS & iPadOS Shortcut)

A lightweight, privacy-friendly Apple Shortcut that extracts your device's **actual Maximum Battery Capacity (%)** and **Charge Cycle Count** directly from Apple's native Analytics log files—no third-party apps required.

## 📥 Download
👉 **[Get the Shortcut via iCloud](https://www.icloud.com/shortcuts/37ecf79e2a254101a4e1ccfb90846165)**

## 🚀 How to Use
1. Open **Settings** on your iPhone or iPad.
2. Go to **Privacy & Security** → **Analytics & Improvements** → **Share Analytics Data (if it is off, turn it On and wait 24 hours)** → **View Analytics Data**.
3. Open the most recent file starting with `Analytics-` (e.g., `Analytics-2026-...`).
4. Tap the **Share** button in the top-right corner and select **Battery health report** from the Share Sheet.
   *(Alternatively, save the log file and run the shortcut directly to pick the file manually.)*

## ⚙️ How It Works
The shortcut reads the plain text of the selected analytics file and uses Regular Expressions (Regex) to extract exact hardware metrics:
- **Battery Health:** `MaximumCapacityPercent"?\s*[:=]\s*(\d+)`
- **Cycle Count:** `CycleCount"?\s*[:=]\s*(\d+)`

If an unsupported file is selected, the shortcut displays an alert (`No battery info in this file`) and exits safely.

## 📸 Shortcut Preview
![Battery health report workflow](preview.png)

## 📦 Backup File
A raw backup copy of the shortcut (`Battery-Health-Report.shortcut`) is archived in this repository. For direct installation on iOS/iPadOS, please use the iCloud link above.

## 📄 License
This project is licensed under the [MIT License](LICENSE).
