# Employee Management API with Fiber and MongoDB

This is a simple Employee Management System implemented using the Fiber web framework for Go and MongoDB as the database. The system provides basic CRUD (Create, Read, Update, Delete) operations for employee records.

## Prerequisites

Before running the application, ensure you have the following installed:

- Go: You can download and install Go from the official website.

- MongoDB: You need a running MongoDB instance. You can install MongoDB locally or use a cloud-hosted solution.

## Getting Started

1. Clone this repository.

```shell
   git clone https://github.com/theafwan/go-fiber-mongo-hrms.git
```

2. Navigate to the project directory.

```shell
   cd go-fiber-mongo-hrms
```

3. Install the required Go packages.

```shell
   go mod tidy
```

4. Run the application.

```shell
   go run main.go
```

By default, the application runs on port `3000`. You can access the API at `http://localhost:3000`.

## API Endpoints

### Get All Employees

- Endpoint: `GET /employee`
- Description: Fetches a list of all employees.
- Response: JSON array containing employee records.

### Create Employee

- Endpoint: `POST /employee`
- Description: Creates a new employee record.
- Request Body: JSON object representing an employee.

```json
{
	"name": "John Doe",
	"salary": 50000,
	"age": 30
}
```

- Response: JSON object of the newly created employee.

### Update Employee

- Endpoint: `PUT /employee/:id`
- Description: Updates an existing employee record by ID.
- Request Body: JSON object with updated employee information.

```json
{
	"name": "Updated Name",
	"salary": 60000,
	"age": 35
}
```

- Response: JSON object of the updated employee.

### Delete Employee

- Endpoint: `DELETE /employee/:id`
- Description: Deletes an employee record by ID.
- Response: Success message.

## Database Configuration

The application uses a local MongoDB instance by default. You can modify the `mongoURI` constant in `main.go` to connect to a different MongoDB database.

## Tech Stack

- [Fiber](https://gofiber.io/): Web framework for Go.
- [MongoDB](https://www.mongodb.com/): NoSQL database.

## License

This project is licensed under the MIT License.
