# To-Do List Frontend

React frontend for the To-Do List application. It uses Vite for local development and builds a static site for deployment.

## Requirements

- Node.js 20 or later
- The To-Do List REST API, or access to the configured hosted API

## Run locally

From this directory, install dependencies and start the development server:

```bash
npm ci
npm run dev
```

Open the local URL printed by Vite (by default, <http://localhost:5173>).

To use a backend other than the hosted default, create `.env.local` in this directory:

```dotenv
VITE_API_URL=http://localhost:8080/api
```

`VITE_API_URL` must include the API base path (`/api`). The provided `.env.example` shows the hosted API URL. Restart Vite after changing environment variables.

## Build

```bash
npm run build
npm run preview
```

The production files are written to `dist/`. The included `vercel.json` supports client-side routes when deploying to Vercel; set the Vercel project root to this repository's root.

## Features

- Create, view, edit, complete, filter, and delete tasks
- Optional descriptions and due dates, with overdue indicators
- Responsive interface with loading, validation, and error states

The API supports `GET` and `POST /api/tasks`, `PUT /api/tasks/{id}`, and `DELETE /api/tasks/{id}`.
