# 📘 Assignment: Building REST APIs with FastAPI

## 🎯 Objective

Build a small REST API with FastAPI that manages a collection of books. You will practice defining HTTP routes, validating request data with Pydantic models, and returning appropriate status codes and responses.

## 📝 Tasks

### 🛠️ Create the API and List Books

#### Description
Create a FastAPI application in `main.py` for managing books. Begin with an in-memory list of at least two sample books and add an endpoint that clients can use to retrieve them.

#### Requirements
Completed program should:

- Create a FastAPI application instance
- Define a `GET /books` endpoint that returns all books as JSON
- Give each book an integer `id`, a `title`, and an `author`
- Return at least two sample books when the application starts
- Run locally with a command such as `uvicorn main:app --reload`


### 🛠️ Add Books with Validation

#### Description
Define a Pydantic model for new books and add an endpoint that accepts JSON data to create a book. The API should assign each new book a unique integer ID rather than requiring the client to provide one.

#### Requirements
Completed program should:

- Define a request model that requires a non-empty `title` and `author`
- Define a `POST /books` endpoint that accepts and validates the request model
- Assign a new unique ID to each created book
- Return the created book as JSON with an HTTP `201 Created` status code
- Return a validation error when required fields are missing or empty

Example request:

```json
{
  "title": "The Hobbit",
  "author": "J. R. R. Tolkien"
}
```


### 🛠️ Implement Book CRUD Operations

#### Description
Complete the API by allowing clients to retrieve, update, and delete one book at a time. Handle IDs that do not exist with a clear `404 Not Found` response.

#### Requirements
Completed program should:

- Define a `GET /books/{book_id}` endpoint that returns one matching book
- Define a `PUT /books/{book_id}` endpoint that validates and replaces a matching book
- Define a `DELETE /books/{book_id}` endpoint that removes a matching book
- Return `404 Not Found` for a book ID that does not exist
- Return a successful delete response with no book data in the response body
- Verify every endpoint using FastAPI's automatically generated `/docs` interface or an HTTP client
