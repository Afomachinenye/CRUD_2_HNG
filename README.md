# CRUD_2_HNG

Simple REST API for Managing People.

This is a simple REST API built using Express.js and MongoDB for CRUD (Create, Read, Update, Delete) operations on a "person" resource.

PREREQUISITES
GETTING STARTED 

Prerequisites
Before you begin, ensure you have met the following requirements:

Node.js installed on your system.
MongoDB installed and running.
Your preferred API testing tool (e.g., Postman or Insomnia).

Getting Started
To get started with this API, follow these steps:

Clone this repository to your local machine
git clone <https://github.com/Afomachinenye/CRUD_2_HNG/tree/master>
cd <CRUD_2_HNG>
Install project dependencies using npm install or yarn install.

Create a .env file in the project root and add the following environment variables:

PORT=4000  # or your preferred port number
DB_URL=mongodb://localhost:27017/<your_database_name>

Start the server.
npm start
# or
yarn start

API Endpoints
Create a new person:
POST /api/

Request Body:
{
  "name": "John Doe"
}

Fetch details of a person: 
GET /api/:id

Update details of a person:
PATCH /api/:id
Request Body:
json
Copy code
{
  "name": "Updated Name"
}
Remove a person:
DELETE /api/:id

Usage
You can use your preferred API testing tool (e.g., Postman) to interact with the API. Below are some sample requests:

Create a new person:
Send a POST request to http://localhost:4000/api/ or   https://hng-crud-api-vzyn.onrender.com/api/ with a JSON body containing the person's name.

Fetch details of a person:
Send a GET request to http://localhost:4000/api/:id or https://hng-crud-api-vzyn.onrender.com/api/:id where :id is the ID of the person you want to retrieve.

Modify details of an existing person:
Send a PATCH request to http://localhost:4000/api/:id or https://hng-crud-api-vzyn.onrender.com/api/:id
with a JSON body containing the updated name.
Remove a person:

Send a DELETE request to http://localhost:4000/api/:id or https://hng-crud-api-vzyn.onrender.com/api/:id where :id is the ID of the person you want to delete.

Troubleshooting
If you encounter any issues or errors, please check the following:

Ensure MongoDB is running and the connection string in the .env file is correct.
Make sure Node.js is installed, and you have installed project dependencies.
Check the API endpoints and request formats in the Usage section.
