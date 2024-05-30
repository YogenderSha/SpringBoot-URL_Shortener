# URL-Shortener

This project is a URL shortener application built with Spring Boot. It provides a simple API to shorten URLs and redirect to the original URLs.

## Project Description

The URL shortener project is designed to create short, easy-to-share URLs from longer URLs. It uses Spring Boot for application configuration and management, Spring Data JPA for database interaction, and H2 as the in-memory database for development and testing.

## Prerequisites

- Java 17
- Maven

## Getting Started

### Clone the Repository

```bash
git clone https://github.com/your-username/URL-Shortener.git
cd URL-Shortener
```

### Build the Project

```bash
mvn clean install
```

### Run the Application

```bash
mvn spring-boot:run
```

The application will start and be accessible at `http://localhost:8080`.

## API Endpoints

### Create a Short URL

- **URL**: `/api/shorten`
- **Method**: `POST`
- **Request Body**: JSON containing the original URL.
- **Response**: JSON containing the shortened URL.

#### Example

Request:

```json
{
  "url": "https://www.example.com"
}
```

Response:

```json
{
  "shortUrl": "http://localhost:8080/abc123"
}
```

### Redirect to Original URL

- **URL**: `/{shortUrl}`
- **Method**: `GET`
- **Response**: Redirects to the original URL.

## Dependencies

- **Spring Boot Starter Data JPA**: For database interaction.
- **Spring Boot Starter Validation**: For request validation.
- **Spring Boot Starter Web**: To build web applications and RESTful services.
- **H2 Database**: An in-memory database for development and testing.
- **Spring Boot Starter Test**: For testing the application.

## Build and Test

To run the tests, use the following command:

```bash
mvn test
```

## Configuration

The application uses H2 in-memory database by default. You can configure the database and other properties in the `application.properties` file.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.
