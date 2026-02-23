# 🎬 The Movie Hub

**The Movie Hub** is a **super lightweight**, fully automated, headless home media system written in modern C++.

It is engineered for **power users** and long-running operation, with an extremely low-overhead architecture designed to run **24/7 with no lag**, even under heavy automation and high torrent throughput.

The system **discovers, validates, downloads, streams, organizes, and plays movies automatically**, with **instant streaming availability** as soon as content becomes available — all controlled remotely via a lightweight web interface.

---

## ✨ Key Features

- ⚡ **Ultra-lightweight C++ architecture** (designed for zero lag)
- 🚀 Fully automated movie discovery & acquisition
- 🎬 **Instant streaming** — search and play as soon as media is available
- 🔍 Torrent aggregation via Jackett
- 🧲 **Custom Smart Torrent engine**
- ⚙️ **High-throughput ingestion**
  - ~**2 torrents per second**
  - ~**7,200 torrents per hour**
  - Stress-tested under sustained load
- 🎥 **Smart Player** (built on **libmpv**) with hardware-aware playback
- 🧠 Advanced duplicate detection (CSV + fuzzy matching)
- 🛡️ Multi-layer content filtering & validation
- 💾 Smart storage guard with hard limits
- 📱 Full remote control (mobile & browser)
- 🌐 Local Netflix-style web UI
- 🧩 Fully modular system design

---

## 🖥️ Screenshots

### Mobile view Homepage 1
![Homepage 1](docs/image_1.png)

### Mobile view Homepage 2
![Homepage 2](docs/image_2.png)

### Mobile view Homepage 3
![Homepage 3](docs/image_3.png)

### Mobile view Homepage 4
![Homepage 4](docs/image_4.png)

### Mobile view Homepage 5
![Homepage 5](docs/image_5.png)

---

## 🧠 Architecture Overview

![System Flow](docs/Architecture-System-Flow.png)

### Core Components

- **Home Control Centre**  
  Hardware detection, orchestration, API layer

- **Full Automation Engine**  
  Discovery, filtering, scheduling, validation

- **Smart Torrent Engine**  
  High-volume torrent ingestion and lifecycle management

- **Smart Player (libmpv)**  
  Streaming and playback optimized for detected hardware

- **Web UI Frontend**  
  Lightweight remote control and monitoring

---

## 🛠️ Tech Stack

- **Language:** C++ (C++23)
- **HTTP:** cpp-httplib, libcurl
- **Torrent Engine:** Custom Smart Torrent
- **Indexer:** Jackett
- **Media:** Smart Player (libmpv)
- **Metadata:** TMDb
- **Parsing:** nlohmann/json
- **Matching:** rapidfuzz
- **Filesystem:** std::filesystem (UTF-8 safe)
- **Frontend:** HTML / CSS / JavaScript

---

## ⚙️ How It Works

1. System starts and **detects hardware, monitors, and available storage**
2. User configuration is loaded:
   - Date ranges (e.g. `2025-01-01 → 2026-01-01`)
   - Genres
   - Ratings and vote thresholds
   - Resolution preferences (4K / 1080p)
   - File size and format rules
   - Storage guard limits
3. Automation engine queries Jackett for candidates
4. Torrents are strictly validated:
   - TMDb metadata matching
   - Title and filename verification
   - Banned word filtering
   - Inappropriate content prevention
5. **Smart Torrent engine ingests torrents at high speed**
6. CSV inventory and fuzzy matching prevent duplicates
7. Movies become **instantly streamable** once available
8. Smart Player selects optimal playback based on detected hardware

---

## 🛡️ Advanced Filtering & Safety

The Movie Hub applies **multi-layer validation** to ensure accuracy and safety:

- TMDb title, year, and metadata matching
- Genre enforcement
- Date-range enforcement
- Banned word filtering
- Title-to-file verification
- Inappropriate content prevention
- **Zero-miss automation** — every qualifying movie is downloaded

---

## 💾 Smart Storage Management

- User-defined storage guard (e.g. max 1TB)
- Hard enforcement — no downloads beyond limit
- Self-managed storage handling
- Designed to prevent disk exhaustion

---

## ⚡ Performance & Efficiency

- Built for **power users**
- Extremely low CPU and memory overhead
- No UI lag under heavy automation
- Optimized for large-scale torrent handling
- Designed for continuous 24/7 operation

---

## 🚧 Project Status

> **Active Development**

Planned enhancements:
- Web-based configuration editor
- User authentication & permissions
- Secure remote access outside LAN
- Multi-device playback targets
- Packaged deployment (mini-PC / appliance)

---

## ⚠️ Legal Notice

This project is intended for **personal media management and educational use only**.  
Users are responsible for complying with all applicable local laws and regulations.

---

## 📜 License

MIT License
