# MyFirstAPI
A Simple RESTful API 
This project demonstrates a simple RESTful API built using Node.js, Express, and MongoDB (Mongoose) to manage subscribers. It provides CRUD (Create, Read, Update, Delete) operations for subscribers.

## Prerequisites

1. Node.js and npm installed on your system
2. MongoDB installed and running locally

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Houssem64/MyFirstApi.git
   ```

2. Navigate to the project directory:
   ```bash
   cd MyFirstApi
   ```

3. Install dependencies:
   ```bash
   npm install
   ```

## Configuration

1. Update the `.env` file with your MongoDB connection details:
   ```bash
   DATABASE_URL=mongodb://localhost:27017/subscriber
   ```

## Running the API

Start the API server using the following command:
```bash
npm DevStart
or
Yarn DevStart
```

This will start the API server on port 3000.

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | /subscribers | Retrieves all subscribers |
| POST | /subscribers | Creates a new subscriber |
| GET | /subscribers/:id | Retrieves a specific subscriber by ID |
| PUT | /subscribers/:id | Updates an existing subscriber |
| DELETE | /subscribers/:id | Deletes a specific subscriber by ID |

## Example Usage

```bash
# Get all subscribers
curl -X GET http://localhost:3000/subscribers

# Create a new subscriber
curl -X POST http://localhost:3000/subscribers -H "Content-Type: application/json" -d '{ "name": "John Doe", "subscribedToChannel": "Tech News" }'

# Get a specific subscriber by ID
curl -X GET http://localhost:3000/subscribers/1

# Update an existing subscriber
curl -X PUT http://localhost:3000/subscribers/1 -H "Content-Type: application/json" -d '{ "name": "Jane Doe", "subscribedToChannel": "News Inc" }'

# Delete a specific subscriber by ID
curl -X DELETE http://localhost:3000/subscribers/1
```

## License

This project is licensed under the MIT License.
