# 🔍 Discovery: Assumptions, Risks, & Open Questions

## 1. Updated Key Assumptions
1. **Kotlin Multiplatform (KMP) Viability:** We assume that KMP is stable enough to share the "Flex Logic" (unit conversion, exercise variations) between the Android app and the Web version.
2. **Unified Data Model:** We assume a single PostgreSQL schema in Supabase can serve both the high-frequency logging of the mobile app and the high-level planning of the web dashboard.
3. **Web Use Case:** We assume the Web version will be used primarily for "Admin/Planning" (creating routines) while Mobile remains the primary tool for "Active Tracking."

---

## 2. Updated Risk Assessment
| Risk | Impact | Mitigation Strategy |
| :--- | :--- | :--- |
| **Web Persistence** | High | Unlike mobile SQLite, web browsers handle local storage differently (IndexedDB). We must ensure the "Offline-First" logic works in-browser. |
| **UI Consistency** | Medium | Using Compose Multiplatform or Flutter to ensure the UI doesn't look "broken" when switching from a 6-inch phone to a 24-inch monitor. |
| **Kotlin/Web Interop** | Medium | If using Compose for Web, we need to monitor the performance of the WASM/JS targets to ensure the "3-tap" speed remains fast. |
| **Auth State Sync** | Low | Ensure Supabase Auth tokens are handled securely and persist across both the mobile app and the web browser. |

---

## 3. Open Questions
- [ ] **Database Logic:** Should the "Variation" logic live in the Kotlin code (shared) or as a Database Function/View in Supabase (SQL)?
- [ ] **Web Framework:** Will we use **Compose Multiplatform** (100% Kotlin) or **KMP + React** (Kotlin for logic, React for Web UI)? 
- [ ] **Offline-Sync Conflict:** If I edit a plan on Web while the Phone is offline, how do we merge those changes when the Phone reconnects? (The "Last Write Wins" vs. "Merge" debate).
- [ ] **PR Parity:** How do we visualize PRs on the Web dashboard vs. the mobile summary to keep them consistent?

---

## 4. The "Parking Lot" (Still Out of Scope)
* Apple Watch/WearOS integration (Deferred to 2027).
* Social sharing or "Gym Buddy" features.
* AI-generated workout plans.