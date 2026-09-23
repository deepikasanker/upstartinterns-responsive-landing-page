# UpStartInterns Task 02 – REST API with Express

## Objective

Build a REST API with Express that supports the four standard operations over one resource.

## Resource

The API uses a `tasks` resource.

### Endpoints

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/api/tasks` | Get all tasks |
| GET | `/api/tasks/:id` | Get one task |
| POST | `/api/tasks` | Create a task |
| PUT | `/api/tasks/:id` | Update a task |
| DELETE | `/api/tasks/:id` | Delete a task |

## Requirements Covered

- GET, POST, PUT and DELETE routes
- JSON request and JSON response
- Correct status codes
- 400 validation responses
- 404 response for missing records
- Express JSON middleware
- API can be tested using Postman or curl

## Run locally

```bash
npm install
npm start
```

The server starts at:

```text
http://localhost:3000
```

## Example JSON for POST

```json
{
  "title": "Learn REST API",
  "status": "pending"
}
```

## Example JSON for PUT

```json
{
  "title": "Learn Express REST API",
  "status": "completed"
}
```

## Test with curl

### GET

```bash
curl http://localhost:3000/api/tasks
```

### POST

```bash
curl -X POST http://localhost:3000/api/tasks -H "Content-Type: application/json" -d "{"title":"Practice Express","status":"pending"}"
```

### PUT

```bash
curl -X PUT http://localhost:3000/api/tasks/1 -H "Content-Type: application/json" -d "{"title":"Updated task","status":"completed"}"
```

### DELETE

```bash
curl -X DELETE http://localhost:3000/api/tasks/1
```
