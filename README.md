# Category API

## Project Description
The Category API is a simple RESTful API built with Go for managing categories. It provides endpoints to create, read, update, and delete categories. The API also includes validation to ensure data integrity and a health check endpoint to verify the server's status.

### Features
- **GET /api/categories**: Retrieve all categories.
- **GET /api/categories/{id}**: Retrieve a category by its ID.
- **POST /api/categories**: Create a new category.
- **PUT /api/categories/{id}**: Update an existing category by its ID.
- **DELETE /api/categories/{id}**: Delete a category by its ID.
- **GET /health**: Check the health status of the API.

### Data Validation
- `Name` is required and cannot exceed 255 characters.
- `Description` cannot exceed 500 characters.

## Testing the Endpoints

### Prerequisites
- Install [Postman](https://www.postman.com/) or use `curl` for testing.
- Ensure the server is running on `localhost:8080`.

### Endpoints

#### 1. **GET /api/categories**
Retrieve all categories.
```bash
curl -X GET http://localhost:8080/api/categories
```

#### 2. **GET /api/categories/{id}**
Retrieve a category by its ID.
```bash
curl -X GET http://localhost:8080/api/categories/1
```

#### 3. **POST /api/categories**
Create a new category.
```bash
curl -X POST http://localhost:8080/api/categories \
-H "Content-Type: application/json" \
-d '{"name": "New Category", "description": "Description of the new category"}'
```

#### 4. **PUT /api/categories/{id}**
Update an existing category by its ID.
```bash
curl -X PUT http://localhost:8080/api/categories/1 \
-H "Content-Type: application/json" \
-d '{"name": "Updated Category", "description": "Updated description"}'
```

#### 5. **DELETE /api/categories/{id}**
Delete a category by its ID.
```bash
curl -X DELETE http://localhost:8080/api/categories/1
```

#### 6. **GET /health**
Check the health status of the API.
```bash
curl -X GET http://localhost:8080/health
```

### Notes
- Replace `{id}` with the actual category ID.
- Ensure the request body for `POST` and `PUT` methods is in JSON format.
- The server must be running to test the endpoints.