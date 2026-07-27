# AGENTS.md

## Project overview
This repository contains a small FastAPI app for Mergington High School activities. The backend lives in [src/app.py](src/app.py) and the browser UI lives in [src/static](src/static).

## Working conventions
- Keep changes focused on the existing FastAPI + static-file structure.
- The app uses in-memory data only. Any new feature should assume state resets when the server restarts unless the request explicitly asks for persistence.
- Preserve the current API shape and route patterns in [src/app.py](src/app.py). Existing endpoints are:
  - `GET /activities`
  - `POST /activities/{activity_name}/signup`
  - `DELETE /activities/{activity_name}/unregister`
- Keep the frontend and API contract aligned. If you change response fields or route behavior, update the client logic in [src/static/app.js](src/static/app.js) as needed.

## Useful commands
- Install dependencies: `pip install -r requirements.txt`
- Run the app from the repository root: `python src/app.py`
- Verify Python syntax after edits: `python -m py_compile src/app.py`

## Key files
- [src/app.py](src/app.py): API routes, activity data, and signup logic.
- [src/static/app.js](src/static/app.js): Browser-side fetch calls and UI updates.
- [src/static/index.html](src/static/index.html): Page structure for the activity UI.
- [src/README.md](src/README.md): Project-specific usage notes.
- [README.md](README.md): Repository-level context and links.

## Guidance for agents
- Prefer small, targeted edits over broad rewrites.
- When adding features, follow the current simple style and avoid introducing new frameworks or databases unless explicitly requested.
- If you need more context, start with the docs in [src/README.md](src/README.md) and [README.md](README.md).
