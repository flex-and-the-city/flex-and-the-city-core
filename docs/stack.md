# Technology Stack: Flex and the City

## 1. Core Frameworks
* **Language:** Java (Logic & Data Processing)
* **Frontend:** [TBD: Jetpack Compose / Flutter / React Native]
* **Database (Cloud):** Supabase (PostgreSQL)
* **Database (Local):** SQLite (for Offline-First logging)

## 2. Why this Stack?
* **Java:** Chosen to reinforce strong typing and object-oriented design patterns.
* **Supabase:** Provides real-time sync and easy authentication without managing a custom server.
* **Offline-First:** Essential for the "Urban Gym" use case where signal is unreliable.

## 3. Architecture Pattern
We will follow the **MVVM (Model-View-ViewModel)** pattern. This separates the Java logic (Model) from the UI (View), making the app easier to test in Q4.

## 4. Open Questions for Q1
- [ ] Should I use Kotlin for the UI (Jetpack Compose) or stick strictly to Java?
- [ ] Does the Supabase Java client support offline caching out of the box?
- [ ] Which UI library offers the fastest "3-tap" logging experience?