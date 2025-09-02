# LyricDisplay Releases

> Official release repository for **LyricDisplay** — a professional real‑time lyric display app for live events, church services, and broadcasts.

**Current Version:** 2.1.1
**Maintained by:** Peter Alakembi
**Built for:** Victory City Media

---

## Quick links

* **Latest release:** [https://github.com/PeterAlaks/lyric-display-updates/releases/latest](https://github.com/PeterAlaks/lyric-display-updates/releases/latest)
* **All releases:** [https://github.com/PeterAlaks/lyric-display-updates/releases](https://github.com/PeterAlaks/lyric-display-updates/releases)
* **Main app repo (Currently private):** [https://github.com/PeterAlaks/lyric-display-app](https://github.com/PeterAlaks/lyric-display-app)

---

## Downloads

Grab the installer for your platform from the **Latest release** page:

* **Windows** – `.exe`
* **macOS** – `.dmg`
* **Linux** – `.AppImage` (or other artefacts provided per release)

> Builds are packaged for one‑click install. No CLI required.

---

## Install & update

1. Download the installer for your OS from the **Latest release**.
2. Run the installer and launch **LyricDisplay**.
3. **Auto‑updates:** the app checks this releases repo for updates and will prompt you to install when a new version is available.

**Uninstall / reinstall:** Installing a newer version over an existing one is supported; your settings are preserved.

---

## How to use

Once installed, you can start using LyricDisplay right away.

### 1. Launch the app

* After installation, open **LyricDisplay** from your desktop or applications folder.
* The control panel will appear where you can load lyrics and configure outputs.

### 2. OBS/VMix integration (same system)

* In OBS or VMix, add a **Browser Source** input.
* For **Output 1**, set the URL to `http://localhost:4000/#/output1`.
* For **Output 2**, set the URL to `http://localhost:4000/#/output2`.
* Set the width to match your video canvas (e.g. 1920) and the height to suit your lyric lines (typically 200–300px).
* Enable **Shutdown source when not visible** for performance and **Refresh browser when active** for reliability.

### 3. OBS/VMix integration (across the network)

If you want to capture outputs from another PC on the same LAN:

⚠️ **Important:** All systems (the machine running LyricDisplay and the OBS/VMix machine) must be connected to the **same network** via LAN cable or Wi‑Fi.

1. **Assign a static IP** to the machine running LyricDisplay:

   * **Windows:**

     * Open *Control Panel → Network & Internet → Network and Sharing Center → Change adapter settings*.
     * Right‑click your active adapter → *Properties* → select *Internet Protocol Version 4 (TCP/IPv4)* → *Properties*.
     * Choose *Use the following IP address* and assign a fixed address (e.g. `192.168.1.100`).
   * **macOS:**

     * Go to *System Preferences → Network*.
     * Select your active interface (Wi‑Fi or Ethernet) → *Advanced* → *TCP/IP*.
     * Set *Configure IPv4* to *Manually* and enter a static address (e.g. `192.168.1.101`).

2. On the OBS/VMix machine, add a **Browser Source** with the following URLs:

   * `http://<Static-IP>:4000/#/output1`
   * `http://<Static-IP>:4000/#/output2`

   Replace `<Static-IP>` with the fixed IP you configured.

### 4. Load lyrics

* Use **File → Load Lyrics File** (or `Ctrl/Cmd + O`).
* Drag and drop `.txt` files directly into the app.
* Create a new song from scratch with **File → New Song** (`Ctrl/Cmd + N`).

### 5. Manage outputs

* Configure **Output 1** and **Output 2** independently in the settings panel.
* Preview outputs with `Ctrl/Cmd + 1` or `Ctrl/Cmd + 2`.
* Toggle the **Display Output** switch to show or hide lyrics on screen.

### 6. Operate live

* Click any lyric line to send it instantly to the output windows.
* Use the search bar to quickly find a song or line.
* Navigate results with **Shift + Up/Down**.
* Refresh or resync outputs if styling changes don’t appear immediately.

---

## Highlights (what you’re getting)

* **Dual independent outputs** with transparent backgrounds (ideal for OBS/VMIX browser sources)
* **Advanced lyric management** with grouped translations and live editing
* **Comprehensive styling** (fonts, colours, shadows, margins, themes)
* **Cross‑platform** with keyboard‑driven workflow and dark mode

> Full feature list and user guide live in the **main app repo** docs.

---

## System requirements (recommended)

* **Windows:** 10 or 11 (64‑bit)
* **macOS:** 12 Monterey or newer (Apple Silicon & Intel)
* **Linux:** Modern 64‑bit distro with glibc ≥ 2.28
* **Hardware:** 8 GB RAM, dual‑display capable GPU for output windows

---

## Verify your download (optional)

Where provided, compare the file’s checksum against the published hash on the release page. On Windows PowerShell:

```powershell
Get-FileHash .\LyricDisplay-Setup-2.1.1.exe -Algorithm SHA256
```

---

## Troubleshooting

* **Output windows not showing in OBS/VMIX:** Refresh/reload the Browser Source; ensure the app is running on the same machine or reachable host.
* **No updates found:** Check your internet connection; confirm you’re running a release build (not a local dev build).
* **Styling not applying:** Use the in‑app "Sync Outputs" control; then refresh your Browser Source in your live software.

See the **main app repo** for deeper troubleshooting guides and FAQs.

---

## Changelog

For detailed changes, use the per‑release notes on the **Releases** page. The high‑level latest:

**v2.1.1**

* Stability and performance improvements
* More reliable real‑time sync
* Enhanced search and navigation
* Polished styling engine

---

## Support

* **Installation or release issues:** open an issue in this releases repo.
* **Feature requests & development issues:** use the **main app repo** issue tracker.

Contact: Peter Alakembi — [https://linktr.ee/peteralaks](https://linktr.ee/peteralaks)

---

## Licence & credits

© 2025 Victory City Media. All rights reserved.

**Developers**
Peter Alakembi (Lead Designer & Developer)
David Okaliwe (Co‑Developer)

---

*LyricDisplay — Powering worship experiences worldwide.*
