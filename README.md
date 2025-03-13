# Student Management API

Made in Early December 2024 as a test to understand how FastAPI works so that I can use it later for my To-Do App.

A simple FastAPI application for managing student records. It allows you to perform CRUD (Create, Read, Update, Delete) operations on student data.

---

## Features

- **Create Student**: Add a new student record.
- **Read Student**: Retrieve student details by ID or name.
- **Update Student**: Modify existing student records.
- **Delete Student**: Remove a student record by ID.

---

## Prerequisites

Before running the application, ensure you have the following:

- **Python 3.7+**: Download and install Python from [python.org](https://www.python.org/).
- **FastAPI**: Install FastAPI using pip:
  ```bash
  pip install fastapi

  How to Run the Application
Clone the Repository:


git clone https://github.com/your-username/your-repo-name.git


Run the Application:


uvicorn myapi:app --reload
Access the API:

Open your browser and go to http://127.0.0.1:8000/. you can all view this in a more UI friendly way by heading to: http://127.0.0.1:8000/docs

Use the following endpoints to interact with the API:

GET /: Returns a welcome message.

GET /get-student/{student_id}: Retrieves student details by ID.

GET /get-by-name/{student_id}: Retrieves student details by name.

POST /create-student/{student_id}: Creates a new student record.

PUT /update-student/{student_id}: Updates an existing student record.

DELETE /delete-student/{student_id}: Deletes a student record by ID.

Example Requests
Create a Student
Endpoint: POST /create-student/2

Body:


Copy
{
  "name": "Alice",
  "age": 16,
  "year": "Year 11"
}
Get a Student by ID
Endpoint: GET /get-student/1

Update a Student
Endpoint: PUT /update-student/1

Body:


Copy
{
  "name": "John Doe",
  "age": 18
}
Delete a Student
Endpoint: DELETE /delete-student/1

Code Structure
app.py: The main FastAPI application file.

Defines endpoints for CRUD operations on student records.

Uses Pydantic models for data validation.

Dependencies
FastAPI

Uvicorn

Pydantic