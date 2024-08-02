# Simple Weather API

## Objective
Create a basic weather API using Python that interacts with a SQL database to store and retrieve weather data. The API allows users to add new weather data and retrieve weather data for a specific city.

## Requirements

### API Endpoints
- `POST /weather`: Add new weather data.
- `GET /weather/{city}`: Retrieve weather data for a specific city.

### Database Schema
- Table: `weather`
- Columns:
  - `id` (Primary Key, Integer, Auto Increment)
  - `city` (Text)
  - `date` (Date)
  - `temperature` (Float)
  - `description` (Text)

### Environment
- Use any HTTP server or API framework of your choice (Flask, aiohttp, FastAPI, LiteStar, or Django REST framework).
- Use SQLite for the database.

## Instructions

### Setup the Project
1. Initialize a Python project with the chosen framework.
2. Set up SQLite database with the required schema.

### API Implementation

#### `POST /weather`
- Request Body:
  ```json
  {
    "city": "CityName",
    "date": "YYYY-MM-DD",
    "temperature": 23.5,
    "description": "Clear sky"
  }
  ```
- Response:
  - `201 Created` on success.
  - `400 Bad Request` on validation error.

#### `GET /weather/{city}`
- Response:
  ```json
  {
    "city": "CityName",
    "date": "YYYY-MM-DD",
    "temperature": 23.5,
    "description": "Clear sky"
  }
  ```
  - `200 OK` with weather data on success.
  - `404 Not Found` if no data is available for the city.

### Testing
- Write basic tests to ensure the API endpoints work as expected.

### Submission
- Provide a GitHub repository link with the complete project.
- Include a README file with instructions on how to set up and run the project locally.

## Evaluation Criteria
- **Correctness**: The API should function as described.
- **Code Quality**: Code should be clean, well-organized, and follow Python best practices.
- **Database Design**: Proper schema design and usage of SQL.
- **Documentation**: Clear and concise README with setup instructions.
- **Error Handling**: Proper error responses and status codes.

Good luck!
