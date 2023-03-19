# Cheap Flights Monitor

This is an application that monitors flight prices and saves them in a database. It uses web scraping to obtain flight prices at a certain interval of time and saves the information to MongoDB.

The application also has an HTTP API that allows you to search for saved flights in the database and get the cheapest flight registered.

## Installation

1. Clone this repository:

```shell
$ git clone https://github.com/your-username/cheap-flights-monitor.git
```
2. Install the dependencies:


```shell
$ cd cheap-flights-monitor
$ npm install
```

3. Configure the environment variables:

```shell
$ cp .env.example .env
$ nano .env
```
4. Start the application:

```shell
$ npm start
```

The application will be available at http://localhost:3000.
## API
### GET /flights

Returns all flights saved in the database.
Query parameters

    origin: filter by flight origin.
    destination: filter by flight destination.
    departureDate: filter by flight departure date in YYYY-MM-DD format.
    arrivalDate: filter by flight arrival date in YYYY-MM-DD format.

### GET /flights/cheapest

Returns the cheapest flight saved in the database.
Configuration

The application uses the following environment variables:

    PORT: the port the HTTP server will run on. The default is 3000.
    MONGODB_URL: MongoDB database connection URL.
    TELEGRAM_TOKEN: Telegram Bot API access token.
    TELEGRAM_CHAT_ID: Telegram chat ID to receive notifications.

Contribution

Feel free to contribute to this project. Just create a pull request with your changes and describe the changes made.