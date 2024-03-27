# Video Service API - Golang

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A RESTful API built with Go using the Gin framework, to handle video-related services including creating and listing video resources.

## Prerequisites

- Go 1.16 or higher. [Download here](https://golang.org/dl/)
- Gin framework

## Getting Started

Clone the repository to your local machine using the following command:

```sh
$ https://github.com/GiorgiMakharadze/video-service-API-golang.git

$ go run server.go
```

## API Endpoints

The CLI tool takes three arguments:

1. `GET /api/videos`: Retrieves a list of all video resources.
2. `POST /api/videos`: Creates a new video resource with the data provided in the request body.
3. `GET /view/videos`: Renders an HTML page displaying all the videos.

## Usage

### Creating videos

To create a video, make a POST request to the /api/videos endpoint with a JSON payload that matches the structure below:

```bash
{
    "title": "Cool gin framework",
    "description": "test",
    "url": "https://www.youtube.com/example/test",
    "author": {
        "firstName": "John",
        "lastName": "Doe",
        "age": 20,
        "email": "test@gmail.com"
    }
}
```

## Notes

The application uses Go Playground Validator for validating the input data. The custom validation function ValidateCoolTitle checks if the word "Cool" is present in the video title.

### Logging

Logs are written to a file named gin.log in the root directory, and also printed to the console.

### Authentication

The /api endpoints are protected with basic authentication. Use the following credentials:

- Username: test
- Password: user
