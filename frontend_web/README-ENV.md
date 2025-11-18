Frontend environment configuration

- This app reads the backend API base URL from a .env file using flutter_dotenv.
- Key:
  BACKEND_BASE_URL=<https-url-of-backend>
- For local development, update frontend_web/.env accordingly. Do not commit secrets.
- Tokens are kept in memory only (SessionProvider). Refresh uses cookie or /auth/refresh if available; no refresh tokens are stored in localStorage/sessionStorage for security.
- On 401 responses, the app redirects to /login.
