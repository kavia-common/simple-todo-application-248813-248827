# Simple Todo Application (React Frontend)

This repository contains a simple Todo web application implemented as a React frontend in `todo_frontend/`. The app is designed to be minimal and easy to run locally.

## Features

The Todo app supports the following user-facing functionality:

- Adding new todo items.
- Marking todo items as completed.
- Deleting todo items.
- Filtering the list by status (all, active, completed).
- Persisting todos locally (saved in the browser via local storage).
- A clean, minimal UI.

## Project Structure

The repository is organized as a single frontend container:

- `todo_frontend/`: React application (Create React App).

## Local Setup

### Prerequisites

- Node.js and npm (a recent LTS version is recommended).

### Install dependencies

From the repository root:

```bash
cd todo_frontend
npm install
```

### Run the app (development)

```bash
cd todo_frontend
npm start
```

This starts the development server (Create React App). By default it runs on port 3000.

## Environment Variables

The frontend reads configuration from `todo_frontend/.env`. Only variables prefixed with `REACT_APP_` are exposed to the browser by Create React App.

The current `.env` in this repo defines the following variables:

- `REACT_APP_API_BASE`: Base URL for API requests (if the UI is configured to call an API).
- `REACT_APP_BACKEND_URL`: Backend base URL (may be the same as `REACT_APP_API_BASE`).
- `REACT_APP_FRONTEND_URL`: Public URL where the frontend is served.
- `REACT_APP_WS_URL`: WebSocket URL (for WS integrations, if used).
- `REACT_APP_NODE_ENV`: Environment label (for example, `development`).
- `REACT_APP_NEXT_TELEMETRY_DISABLED`: Telemetry flag (not typically used by CRA, but present in the environment).
- `REACT_APP_ENABLE_SOURCE_MAPS`: Whether source maps should be enabled.
- `REACT_APP_PORT`: Port for the dev server (commonly `3000`).
- `REACT_APP_TRUST_PROXY`: Whether the app should trust proxy headers (if applicable).
- `REACT_APP_LOG_LEVEL`: Logging level hint (if used by the app).
- `REACT_APP_HEALTHCHECK_PATH`: Health check path (if used by surrounding tooling).
- `REACT_APP_FEATURE_FLAGS`: Feature flag configuration (stringified).
- `REACT_APP_EXPERIMENTS_ENABLED`: Toggle for experiments.

If you change `todo_frontend/.env`, you typically need to restart `npm start` for the new values to be picked up.

## Preview / Access

- Local development URL: `http://localhost:3000`
- In the hosted preview environment, the frontend container is exposed on port `3000` via the platform’s provided URL.

## Useful Scripts

Run these from `todo_frontend/`:

- `npm start`: Start the dev server.
- `npm test`: Run tests.
- `npm run build`: Create a production build in `todo_frontend/build`.

## Notes

This repository currently contains only the frontend container. There is no database container unless explicitly added.
