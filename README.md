# FastAPI Todo Application

A simple RESTful API for managing todo items built with FastAPI and SQLite.

## Features

- Create, read, update, and delete todo items
- SQLite database for data persistence
- Automatic API documentation with Swagger UI
- Input validation using Pydantic models

## Installation

1. Clone the repository:

```bash
git clone <your-repository-url>
cd bugs-and-glitches
```

2. Create a virtual environment and activate it:

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

## Running the Application

1. Start the server:

```bash
python main.py
```

2. The API will be available at `http://localhost:8000`
3. Access the API documentation at `http://localhost:8000/docs`

## API Endpoints

- `GET /todos` - Retrieve all todo items
- `POST /todos` - Create a new todo item
- `GET /todos/{todo_id}` - Retrieve a specific todo item
- `PUT /todos/{todo_id}` - Update a specific todo item
- `DELETE /todos/{todo_id}` - Delete a specific todo item

## Example Usage

### Create a Todo Item

```bash
curl -X POST "http://localhost:8000/todos" \
     -H "Content-Type: application/json" \
     -d '{"title": "Learn FastAPI", "description": "Complete the tutorial", "completed": false}'
```

### Get All Todo Items

```bash
curl "http://localhost:8000/todos"
```
