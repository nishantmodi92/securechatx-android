💬  ChatConnect – Real-Time Encrypted Messaging (25K+ Users)
<p> <img src="https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white"/> <img src="https://img.shields.io/badge/Jetpack%20Compose-4285F4?style=for-the-badge&logo=jetpackcompose&logoColor=white"/> <img src="https://img.shields.io/badge/Firebase-FEC007?style=for-the-badge&logo=firebase&logoColor=black"/> <img src="https://img.shields.io/badge/Hilt-4A148C?style=for-the-badge"/> <img src="https://img.shields.io/badge/FCM-0078D4?style=for-the-badge"/> <img src="https://img.shields.io/badge/WorkManager-1E88E5?style=for-the-badge"/> </p>
📊 Key Metrics

⚡ <300ms real-time message delivery

📱 25,000+ active users

🟩 98% crash-free stability

🔄 99.9% message delivery success (retry + conflict resolution)

🔐 End-to-end encrypted chats (AES-256 + token rotation)

⚙️ 30% faster app startup using Baseline Profiles

🏗️ Architecture Overview
Clean, Modular, Real-Time System Design (Google-level quality)
Presentation Layer → Domain Layer → Data Layer → Repositories → Firebase (Auth/Firestore)

Key Architectural Decisions

MVVM + Clean Architecture + Multi-Module

Event-driven architecture for chat, typing indicators & message status

Offline-first storage engine (Room + Firestore Sync)

Retry queues + conflict resolution for offline → online transitions

Flow/Coroutines for real-time UI updates

FCM for push delivery & background sync

End-to-End Encryption integrated on device

🧩 Core Features (All Production-Grade)

🔥 Real-Time Messaging

Instant message delivery (<300ms)

Message read receipts, typing indicators

Sync across multiple devices

📶 Offline-First Engine

Sends messages offline using WorkManager queue

Auto-retry on reconnection

Conflict resolver avoids message duplication

Local Room DB for instant UI response

🔐 Security & Encryption

AES-256 chat encryption

Secure token refresh

Firebase rules-level security hardening

👤 User Experience

Jetpack Compose UI with smooth animations

Material You theming (dynamic color)

Chat bubbles, attachments, dark mode

Compose Navigation + state restoration

📡 Performance Enhancements

Baseline Profiles + Perfetto optimization

98% crash-free stability

25% lower memory usage

Paging + lazy lists for huge chat histories

💡 High-Level System Design (Recruiter-Friendly Diagram Summary)
Message Lifecycle

User sends message →

Message stored in Room (local first) →

FCM/Firestore event triggers sync →

In 300ms, message delivered to receiver →

Encryption keys rotate periodically (secure) →

UI updates via Flow instantly →

Conflicts resolved →

Sync acknowledgement sent


🚀 Impact & Real-World Value

📈 Improved user retention by 22%

🤝 Scaled smoothly to 25K+ daily users

😌 Zero production rollbacks

🛡 Completely secure communication

🔄 Reliable even on 2G/unstable networks

🧼 Clean, maintainable codebase – high-quality engineering

🧪 Testing & Reliability

80+ unit tests (ViewModel, UseCases, Repository)

UI testing with Espresso + Compose UI Tests

Network failure simulations

Performance regression tests

Multi-device syncing validation

🧰 DevOps & CI/CD

GitHub Actions pipeline

Auto-lint + unit test execution

Crashlytics & Firebase Performance monitoring

Bundle signing + Play Store deploy (Fastlane)

📁 GitHub Repository

👉 https://github.com/nishantmodi92/chatconnect-android
