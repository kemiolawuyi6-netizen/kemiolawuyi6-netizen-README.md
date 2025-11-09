# NaijaTeach — System Architecture

## Frontend — Mobile App
- Framework: Flutter
- Responsibilities:
  - display micro-lessons
  - handle user interactions
  - store progress offline
  - sync with backend when online

## Backend — Application Server
- Node.js or Firebase Functions
- Responsibilities:
  - store lesson content
  - authenticate users
  - receive user progress data
  - deliver analytics for visibility tracking

## Database
- On-device: SQLite (for offline-first mode)
- Cloud: Firestore / PostgreSQL
- Responsibilities:
  - maintain lesson states
  - store activity logs
  - enable cross-device progress recovery

## Communication
- Flutter app → REST API → Backend
- Offline:
  - writes to SQLite
  - syncs to cloud when online

## Technical Feasibility
- **Offline-first** ensures adults in low-connectivity areas can learn
- **Cross-platform Flutter** reduces dev cost + single codebase
- **Decodable lessons** makes content modular and scalable
- **Backend analytics** supports amplification & research insights

This architecture allows NaijaTeach to scale quickly, support multiple languages, and reach adults in real Nigerian environments.
