# chirpy

Chirpy is a simple web application that provides a RESTful API for managing user accounts and chirps (short messages). This project is built using Go and includes features such as user authentication, JWT-based authorization, and webhook handling.

## Table of Contents

- Installation
- Usage
- API Endpoints
- Environment Variables
- License

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/calebbramel/chirpy.git
    cd chirpy
    ```

2. Install dependencies:
    ```sh
    go mod tidy
    ```

3. Create a `.env` file in the root directory and add the following environment variables:
    ```env
    JWT_SECRET=your_jwt_secret
    POLKA_KEY=your_polka_key
    ```

4. Build the project:
    ```sh
    go build -o chirpy
    ```

## Usage

1. Run the application:
    ```sh
    ./chirpy
    ```

2. The server will start on port 8080 by default. You can access the application at `http://localhost:8080`.

## API Endpoints

- `GET /api/healthz` - Check the health of the application.
- `GET /api/reset` - Reset the page view count.
- `POST /api/polka/webhooks` - API Key verification for account upgrades.
- `POST /api/revoke` - Revoke a token.
- `POST /api/refresh` - Refresh a token.
- `POST /api/login` - Log in a user.
- `POST /api/users` - Create a new user.
- `PUT /api/users` - Update an existing user.
- `DELETE /api/chirps/{chirpID}` - Delete a chirp.
- `POST /api/chirps` - Create a new chirp.
- `GET /api/chirps` - Retrieve all chirps.
- `GET /api/chirps/{chirpID}` - Retrieve a specific chirp.
- `GET /admin/metrics` - Get application metrics.

## Environment Variables

- `JWT_SECRET` - Secret key for JWT authentication.
- `POLKA_KEY` - API key for user upgrade processing.
