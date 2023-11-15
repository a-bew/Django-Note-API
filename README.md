# Note API

This is a simple note API built with Django Rest Framework.

## Endpoints

### Get all notes

`GET /notes/`

Returns JSON array of all note objects.

### Get a single note

`GET /notes/:id`

Returns JSON of note object matching `:id`.

### Create a new note

`POST /notes/create/`

Creates a new note. Expects JSON request body with a `body` field for the note body text.

### Update an existing note

`PUT /notes/:id/update/`

Updates an existing note matching `:id`. Expects JSON request body with a `body` field for the updated note body text.

### Delete a note

`DELETE /notes/:id/delete/`

Deletes note matching `:id`.

## Example Requests

### Get all notes

```bash
curl https://example.com/notes/
```

### Get note with ID 123

```bash
curl https://example.com/notes/123
```

### Create a new note

```bash
curl -X POST -H "Content-Type: application/json" -d '{"body": "This is a new note"}' https://example.com/notes/create/

```

### Update note 123

```bash
curl -X PUT -H "Content-Type: application/json" -d '{"body": "This note has been updated"}' https://example.com/notes/123/update/

```
