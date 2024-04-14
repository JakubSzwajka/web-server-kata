
# Weather Data Server Kata

This project is designed to be a comprehensive programming kata across multiple languages, focusing on building a web server that serves weather data. It incorporates several key aspects of modern backend development, including web server creation, API interaction, database operations, authentication, and containerization.

## Project Overview

Build a simple web server that:
- Listens on a specified port.
- Handles HTTP GET requests to fetch weather data for a specified city.
- Incorporates user management and authentication.
- Utilizes PostgreSQL for storing user data and optionally weather queries.
- Is containerized for easy setup and deployment.

## Features

### Core Features
- **Web Server & API:** Setup a basic server with endpoints for user signup/login and fetching weather data.
- **Dynamic URL Parsing:** Extract city names from the URL for the weather data endpoint.
- **Mock/External Weather API:** Simulate or actually fetch weather data from an external source and return it as JSON.
- **JSON Response:** Respond with weather data in a predefined JSON format.

### Authentication & Security
- **User Signup/Login:** Implement endpoints for user registration and authentication.
- **JWT Authentication:** Secure the weather data endpoint with JWT tokens.
- **Password Hashing:** Ensure passwords are securely stored.

### Database Operations
- **PostgreSQL Integration:** Connect to a PostgreSQL database for user management.
- **CRUD Operations:** Implement basic CRUD operations for user data.

### Dockerization
- **Containerize Application:** Create a Dockerfile for the server.
- **Database Container:** Use PostgreSQL as a Docker container.
- **Docker Compose:** Setup Docker Compose to orchestrate the application and database containers.

## Requirements

- **Languages:** Choose from Python, JavaScript (Node.js), Rust, C++, or Go.
- **Database:** PostgreSQL.
- **Authentication:** JWT for token generation and verification.
- **Containerization:** Docker and Docker Compose for deployment.

## Expected JSON Response Format

```json
{
  "city": "CityName",
  "temperature": "22°C",
  "condition": "Sunny",
  "humidity": "55%"
}
```

## Additional Challenges

- Implement caching for weather data to reduce API calls.
- Add more detailed error handling and logging.
- Expand the user model to include more details and possibly user preferences for weather data.

## Project Structure

- POST /signup: User registration endpoint.
- POST /login: User login endpoint, returns JWT.
- GET /weather/{city}: Protected endpoint to fetch weather data, requires JWT.
