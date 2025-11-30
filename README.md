# ChatConnect – Real-Time Chat & Messaging App

## 🚀 Overview
ChatConnect is a high-performance, real-time messaging app built using Kotlin, Jetpack Compose, WebSockets, and a fully offline-first architecture.  
It is designed to handle instant message delivery, synchronization conflicts, and secure encrypted communication even on unstable networks.

This project demonstrates:
- Real-time bidirectional messaging
- WebSocket-based live updates
- Full offline mode with mutation queues
- AES-256 encryption for secure chats
- Modular Clean Architecture in production style

---

## 🛠 Tech Stack
-### Tech & Tools

![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)
![Coroutines](https://img.shields.io/badge/Coroutines-00BFFF?style=for-the-badge&logo=kotlin&logoColor=white)
![Flows](https://img.shields.io/badge/Flows-FF69B4?style=for-the-badge&logo=kotlin&logoColor=white)
![Jetpack Compose](https://img.shields.io/badge/Jetpack%20Compose-4285F4?style=for-the-badge&logo=android&logoColor=white)
![WebSockets](https://img.shields.io/badge/WebSockets-8A2BE2?style=for-the-badge&logo=websocket&logoColor=white)
![Room Database](https://img.shields.io/badge/Room-FF6F61?style=for-the-badge&logo=sqlite&logoColor=white)
![WorkManager](https://img.shields.io/badge/WorkManager-00C853?style=for-the-badge&logo=android&logoColor=white)
![Hilt DI](https://img.shields.io/badge/Hilt-D32F2F?style=for-the-badge&logo=android&logoColor=white)
![AES-256 + Keystore](https://img.shields.io/badge/AES--256_Keystore-FF9800?style=for-the-badge&logo=lock&logoColor=white)
![Clean Architecture](https://img.shields.io/badge/Clean%20Architecture-03A9F4?style=for-the-badge&logo=architecture&logoColor=white)


---

## 🧩 Architecture

app
│
├── core/
│ ├── network/ (WebSocket, API)
│ ├── storage/ (Room, Preferences)
│ ├── encryption/ (AES, Keystore)
│ └── utils/
│
├── data/
│ ├── repository/
│ ├── datasource-local/
│ └── datasource-remote/
│
├── domain/
│ ├── model/
│ └── usecase/
│
└── feature-chat/
├── ui/
├── viewmodel/
└── model/


---

## ⭐ Core Features
- One-to-one real-time chat  
- Message delivery receipts (Sent, Delivered, Read)  
- Offline mode with queued messages  
- Automatic WorkManager sync  
- Local encryption for messages  
- Optimized Compose UI for large threads  

---

## 🗄 Database Schema Example
```kotlin
@Entity(tableName = "messages")
data class MessageEntity(
  @PrimaryKey val id: String,
  val chatId: String,
  val body: String,
  val senderId: String,
  val timestamp: Long,
  val status: Int
)

🔄 Background Sync Example
class MessageSyncWorker (...) : CoroutineWorker(...) {
    override suspend fun doWork(): Result {
        repo.syncPendingMessages()
        return Result.success()
    }
}

🔒 Security

AES-GCM encryption for message bodies

Keystore-protected master key

TLS-only communication

Token rotation + strict validation


📈 Performance Highlights

Recycler-less inbox (Compose Lazy Lists)

Local caching for zero-latency messages

Optimized WebSocket reconnection strategy

Baseline Profiles for faster startup

🚀 Setup

Open in Android Studio

Configure WebSocket URL in NetworkModule

Run on device or emulator


📡 System Design Summary

Realtime Layer: WebSocket

Offline Layer: Room + Mutation Queue

Sync Layer: WorkManager periodic + on-demand

Conflict Handling: Timestamp + clientSeq
