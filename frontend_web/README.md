# Frontend (Flutter) - Env Integration

This minimal scaffold wires the app to read BACKEND_BASE_URL from a `.env` file using `flutter_dotenv`.

Setup:
1) Copy `.env.example` to `.env`
2) Set:
   BACKEND_BASE_URL=https://vscode-internal-23122-beta.beta01.cloud.kavia.ai:3001

Notes:
- `pubspec.yaml` registers `.env` under assets so it's bundled for debug/web.
- `lib/services/api_client.dart` exposes `ApiClient.baseUrl` and helpers (getJson/postJson/etc.).
- `lib/main.dart` loads `.env` before `runApp` and displays the configured base URL.

Alignment with containers:
- backend_api/.env -> DB_URL=sqlite:///./app.db, CORS_ORIGINS includes https://appetize.io
- database_postgres/.env -> SQLITE_DB=./app.db
- frontend_web/.env -> BACKEND_BASE_URL=https://vscode-internal-23122-beta.beta01.cloud.kavia.ai:3001
