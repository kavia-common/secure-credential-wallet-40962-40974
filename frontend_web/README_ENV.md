Frontend environment usage

- Define BACKEND_BASE_URL in .env to point to FastAPI service (e.g., http://localhost:8000).
- In your API client or service layer, read BACKEND_BASE_URL from the environment and construct endpoint URLs accordingly.
- For feature-gated UI flows, parse FEATURE_FLAGS (comma-separated) as needed.
