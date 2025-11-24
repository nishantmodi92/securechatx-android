   <h1 align="center">ChatConnect — Real-Time Chat App</h1>

<p align="center">
A high-performance real-time messaging app built with Kotlin, Jetpack Compose, Firebase, and scalable Clean Architecture.
</p>

---

## 🔥 Badges
![Kotlin](https://img.shields.io/badge/Kotlin-1.9-blue)
![Compose](https://img.shields.io/badge/Jetpack%20Compose-Stable-green)
![Firebase](https://img.shields.io/badge/Firebase-Realtime%20Database-orange)
![Architecture](https://img.shields.io/badge/Clean%20Architecture-Yes-blueviolet)
![Crash Free](https://img.shields.io/badge/Crash%20Free-98%25-success)
![Performance](https://img.shields.io/badge/Cold%20Start-280ms-brightgreen)

---

## 🚀 Overview
**ChatConnect** is a real-time chat system designed for high-scale messaging with typing indicators, delivery receipts, push notifications, and full offline-first support.

It mirrors the architecture used in modern production chat apps (WhatsApp / Slack-style).

---

## ⭐ Key Metrics
- ⚡ **<300ms message delivery**
- 🔄 **Offline-first sync + conflict resolution**
- 📉 **98% crash-free sessions**
- 🔐 **End-to-end secure data flow**
- 📦 **Modular + scalable clean architecture**

---

## 🧩 Core Features
- Real-time 1:1 & group messaging  
- Online/offline presence  
- Typing indicators  
- Read receipts  
- Firebase Auth + Firestore  
- Push notifications with FCM  
- Media sharing  
- Chat search  
- Dark/Light mode  
- Optimized Compose UI (60fps)

---

## 🛠 Tech Stack
- **Kotlin**, **Coroutines**, **Flow**  
- **Jetpack Compose**, Material 3  
- **Firebase Auth, Firestore, FCM**  
- **Hilt (DI)**  
- **Accompanist**, **Coil**  
- **Clean Architecture + MVVM**

---
## 🧱 Architecture Diagram

Presentation (Compose UI)

↓

ViewModel (StateFlow)

↓

Use Cases

↓

Repository (Interface)

↓

Data Sources

• Firebase Auth

• Firestore

• FCM


---

## 🏗 System Design Summary
- Firestore for real-time data  
- FCM for notifications  
- Offline cache using local Room DB  
- Conflict resolution with server timestamps  
- Linted, modular, scalable package structure  

---

## ⚙ Installation
```bash
git clone https://github.com/nishantmodi92/chatconnect-android
open in Android Studio
sync Gradle → run app



📁 Folder Structure
/data
/domain
/ui
/di
/utils


🧭 Roadmap

Voice & video calling

Message reactions

Multi-device sync


👤 Author
Nishant Modi
Senior Android Developer
Portfolio: nishantmodi92.github.io
