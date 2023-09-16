# CRUD_2_HNG


API Documentation

This DOCUMENTATION.md file provides a reference for using the API, understanding the expected request and response formats, and highlights any limitations and assumptions. Users and developers can use this documentation to interact effectively with the API.


Request Format
For all endpoints that accept JSON data (e.g., POST and PUT requests), the request format should be as follows:
{
  "name": "John Doe"
}

Response Format
All API responses will follow this format:
{
  "status": true,
  "data": {
    "name": "John Doe",
    "_id": "1234567890"  // Unique identifier
  }
  
}

Endpoints
1. Create a new person
Endpoint: POST /api/
Request Format:
{
  "name": "John Doe"
}

Expected Response:
{
  "status": true,
  "data": {
    "name": "John Doe",
    "_id": "1234567890"
  }
}

2. Fetch details of a person
Endpoint: GET /api/:id
Expected Response (if person found):
{
  "status": true,
  "data": {
    "name": "John Doe",
    "_id": "1234567890"
  }
}
Expected Response (if person not found):
{
  "status": false,
  "error": "User not found"
}

3. Modify details of an existing person
Endpoint: PATCH /api/:id
Request Format:
{
  "name": "Updated Name"
}
Expected Response (if person found):
{
  "status": true,
  "data": {
    "name": "Updated Name",
    "_id": "1234567890"
  }
}

4. Remove a person
Endpoint: DELETE /api/:id
Expected Response (if person found and deleted):
{
  "status": true,
  "message": "User deleted successfully"
}
Expected Response (if person not found):
{
  "status": false,
  "error": "User not found"
}

Sample API Usage: 

Create a new person
curl -X POST -H "Content-Type: application/json" -d '{"name": "John Doe"}' http://localhost:4000/api/ or https://hng-crud-api-vzyn.onrender.com/api/

Fetch details of a person
curl http://localhost:4000/api/1234567890 or https://hng-crud-api-vzyn.onrender.com/api/1234567990

Modify details of an existing person
curl -X PATCH -H "Content-Type: application/json" -d '{"name": "Updated Name"}' http://localhost:4000/api/1234567890 or 
https://hng-crud-api-vzyn.onrender.com/api/1234567990

Remove a person
curl -X DELETE http://localhost:4000/api/1234567890

Known Limitations and Assumptions
•	This API assumes that the unique identifier for a person is their MongoDB-generated _id.
•	It does not handle complex validation and authentication mechanisms for simplicity.
•	Error handling is minimal and may not cover all possible scenarios.

Local Setup and Deployment
To set up and deploy the API locally or on a server, follow the instructions in the README.md file of this project.
