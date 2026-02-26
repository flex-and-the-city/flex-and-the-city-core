# Technology Stack: Flex and the City

## 1. Core Frameworks
* **Language:** Kotlin (Primary)
* **Frontend:** [TBD: Flutter / Compose Multiplatform / React Native]
* **Platform Target:** Cross-platform (Android, iOS, and Web)
* **Database (Cloud):** Supabase (PostgreSQL + Auth)
* **Database (Local):** SQLite (for Offline-First logging)

## 2. Why this Stack?
* **Kotlin:** Modern, concise, and safe. It provides excellent interoperability with Java while offering superior features like Coroutines for smooth background data syncing.
* **Supabase:** Handles the heavy lifting of real-time database management and user authentication.
* **Multi-platform:** Adding a **Web version** allows for easier workout planning on a desktop, while the mobile app handles the heavy lifting inside the gym.
* **Offline-First:** Essential for "Urban Gym" scenarios. Data is captured locally and synced to the cloud when a connection is available.

## 3. Architecture Pattern
We will follow the **MVVM (Model-View-ViewModel)** pattern. 
* **Model:** Kotlin data classes and Supabase entities.
* **View:** Declarative UI (Compose or Flutter widgets).
* **ViewModel:** Handles the logic of unit conversion (kg/lbs) and exercise variations.

## 4. Multi-platform Feasibility (Web + Mobile)
To achieve a Web version alongside Mobile, we are evaluating:
1. **Flutter:** High consistency across web/mobile; Dart is very similar to Java/Kotlin.
2. **Compose Multiplatform:** Allows us to keep everything in 100% Kotlin, though Web support is currently in a "stable-evolving" state.
3. **React Native:** Strongest for web (React), but moves us away from the Kotlin-heavy logic.

## 5. Open Questions for Q1
- [ ] **Framework Choice:** Which framework provides the most stable "Web + Mobile" experience using Kotlin/Dart?
- [ ] **Local DB on Web:** Since SQLite is a file-based system, what is the best equivalent for local storage on a Web browser (IndexedDB)?
- [ ] **Auth Sync:** How will the login session persist seamlessly between the web dashboard and the mobile tracker?