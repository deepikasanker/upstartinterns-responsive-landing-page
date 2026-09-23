# UpStartInterns Task 03 – CRUD App on a Database

A full-stack CRUD assignment manager built with Express, SQLite, HTML, CSS and JavaScript.

## Requirements Covered

- Designed database schema using SQLite
- Frontend communicates with an Express REST API
- GET, POST, PUT and DELETE operations
- Input validation before database storage
- Persistent data stored in `tasks.db`
- Changes survive server/browser restart
- Responsive frontend
- Edit, complete and delete actions

## Project Structure

```text
upstartinterns-task03-crud-database/
├── server.js
├── package.json
├── README.md
├── .gitignore
└── public/
    ├── index.html
    ├── style.css
    └── app.js
```

## Database Schema

The `tasks` table contains:

- `id` – primary key
- `title` – assignment title
- `subject` – subject/category
- `priority` – Low, Medium or High
- `completed` – 0 or 1
- `created_at` – creation timestamp

The database is automatically created as `tasks.db` when the server starts.

## Run

```bash
npm install
npm start
```

Open:

```text
http://localhost:3000
```

## API Endpoints

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/api/tasks` | Read all tasks |
| GET | `/api/tasks/:id` | Read one task |
| POST | `/api/tasks` | Create a task |
| PUT | `/api/tasks/:id` | Update a task |
| DELETE | `/api/tasks/:id` | Delete a task |

## Persistence Test

1. Add an assignment.
2. Stop the server.
3. Start the server again.
4. Open the application.
5. The assignment remains because it is stored in SQLite.
