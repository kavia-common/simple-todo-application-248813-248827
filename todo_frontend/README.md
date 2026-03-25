# Todo Frontend (React)

This folder contains the React frontend for a simple Todo application. The UI is intended to be minimal while supporting the core Todo interactions.

## Features

The Todo app supports:

- Adding new todo items.
- Marking todo items as completed.
- Deleting todo items.
- Filtering (all, active, completed).
- Persisting todos in the browser using local storage.

## Local Development

### Prerequisites

- Node.js and npm.

### Install

From this directory:

```bash
npm install
```

### Run (development)

```bash
npm start
```

Then open:

- http://localhost:3000

## Environment Variables

This app uses Create React App, so only environment variables prefixed with `REACT_APP_` are available in the frontend code.

The environment variables are defined in `.env` in this folder. The current `.env` includes:

- `REACT_APP_API_BASE`: Base URL for API requests (if used by the UI).
- `REACT_APP_BACKEND_URL`: Backend base URL (may be the same as `REACT_APP_API_BASE`).
- `REACT_APP_FRONTEND_URL`: Public URL where the frontend is served.
- `REACT_APP_WS_URL`: WebSocket URL (for WS integrations, if used).
- `REACT_APP_NODE_ENV`: Environment label (for example, `development`).
- `REACT_APP_NEXT_TELEMETRY_DISABLED`: Telemetry flag (present in the environment).
- `REACT_APP_ENABLE_SOURCE_MAPS`: Whether source maps should be enabled.
- `REACT_APP_PORT`: Port for the dev server (commonly `3000`).
- `REACT_APP_TRUST_PROXY`: Whether to trust proxy headers (if applicable).
- `REACT_APP_LOG_LEVEL`: Logging level hint (if used by the app).
- `REACT_APP_HEALTHCHECK_PATH`: Health check path (if used by tooling).
- `REACT_APP_FEATURE_FLAGS`: Feature flag configuration (stringified).
- `REACT_APP_EXPERIMENTS_ENABLED`: Toggle for experiments.

After editing `.env`, restart the dev server to ensure changes take effect.

## Build and Test

- Build for production:

  ```bash
  npm run build
  ```

- Run tests:

  ```bash
  npm test
  ```

## Preview

In the platform preview environment, the `todo_frontend` container is served on port `3000` via the provided preview URL.
