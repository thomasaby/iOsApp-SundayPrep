# SundayPrep 📖⛪

**SundayPrep** is a personal iOS app designed to help prepare for Sunday worship by delivering a summarized reminder of church announcements and the upcoming sermon scripture every Sunday morning.

This project is intentionally built as a **learning-first iOS application**, focusing on clean architecture, native Apple APIs, and incremental feature development.

---

## ✨ Project Goals

- Learn native iOS development using **Swift** and **SwiftUI**
- Build a **local-first** app with no initial backend dependency
- Deliver a meaningful weekly notification at a predictable time
- Gradually evolve toward automation using email ingestion and AI summarization

---

## 🧠 Core Concept

Every Friday, the church sends an email with:
- General announcements
- The upcoming sermon topic
- Scripture reference

This app ensures that:
- The key information is **saved**
- A reminder is delivered **every Sunday at 8:00 AM**
- The user sees a **concise summary**, not the full email

---

## 🏗️ Architecture Overview

### Phase 1: Local iOS App (Current Focus)
- SwiftUI-based user interface
- Manual input of announcements and sermon info
- Local storage on device
- Local notifications scheduled via iOS system APIs
- No backend required

### Phase 2: Automation (Planned)
- Dedicated mailbox for church emails
- External script/service reads emails
- AI model summarizes content into structured data
- App consumes structured data only (no email or AI logic inside app)

---

## 🧱 App Structure (Phase 1)

SundayPrep/
├── SundayPrepApp.swift # App entry point
├── ContentView.swift # Main UI
├── NotificationManager.swift# Notification scheduling logic
├── Models/ # Data models (future)
├── Services/ # Storage & processing logic


---

## 🔔 Key Features (Phase 1)

- ✍️ Manual entry of:
  - Announcements
  - Sermon topic
  - Scripture reference
- 💾 Local persistence (UserDefaults / AppStorage)
- ⏰ Weekly local notification every Sunday at 8:00 AM
- 📱 Simple, distraction-free interface

---

## 🗺️ Roadmap

### Phase 1 — Foundation (In Progress)
- [x] Xcode project setup
- [x] SwiftUI form-based UI
- [x] Notification permission handling
- [x] Sunday notification scheduling
- [ ] Persistent local storage
- [ ] Improved date logic (always “next Sunday”)

### Phase 2 — Intelligence
- [ ] Text parsing helpers (scripture detection)
- [ ] Announcement summarization
- [ ] UI polish & accessibility improvements

### Phase 3 — Automation
- [ ] Dedicated email inbox
- [ ] Email ingestion script (Python or Swift)
- [ ] AI-powered summarization
- [ ] Structured JSON output
- [ ] App sync mechanism

---

## 🔐 Design Principles

- **Local-first**: The app functions fully offline
- **No secrets in the app**: API keys and email credentials stay outside iOS
- **Separation of concerns**:
  - UI displays data
  - Services perform logic
  - System APIs handle scheduling
- **Incremental complexity**: Each phase builds on the last

---

## 🛠️ Tech Stack

### iOS App
- Swift
- SwiftUI
- UserNotifications
- UserDefaults / AppStorage

### Automation (Future)
- Python or Swift scripting
- IMAP email access
- AI summarization (LLM)
- JSON-based data exchange

---

## 📚 Learning Objectives

By completing this project, the following skills will be developed:

- Native iOS app architecture
- SwiftUI state management
- iOS notification system
- App lifecycle awareness
- Clean separation between client and automation logic
- Real-world incremental software design

---

## 🚧 Status

This project is actively under development and intentionally evolving.

---

## 📄 License

Personal project. Not intended for commercial distribution.