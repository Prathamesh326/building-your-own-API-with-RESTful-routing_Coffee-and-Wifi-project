# Cafe & Wifi API

Welcome to the Cafe & Wifi API! This project provides a RESTful API for managing cafes with wifi and other amenities.

## Features

- **Get a Random Cafe**: Retrieve a random cafe from the database.
- **Get All Cafes**: Retrieve a list of all cafes in the database.
- **Search Cafes by Location**: Search for cafes in a specific location.
- **Add a New Cafe**: Add a new cafe to the database.
- **Update Cafe Price**: Update the coffee price of a specific cafe.
- **Delete a Cafe**: Delete a cafe from the database.

## API Documentation

For detailed information about the API endpoints and how to use them, please refer to the [API documentation](https://documenter.getpostman.com/view/37348907/2sA3kd9cbq).

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/Prathamesh326/building-your-own-API-with-RESTful-routing_Coffee-and-Wifi-project.git
    cd building-your-own-API-with-RESTful-routing_Coffee-and-Wifi-project
    ```

2. Install the required packages:
    ```bash
    # On Windows
    python -m pip install -r requirements.txt
    
    # On MacOS
    pip3 install -r requirements.txt
    ```

3. Run the application:
    ```bash
    python main.py
    ```

## Database

The project uses SQLite for the database. The database configuration is specified in `app.config['SQLALCHEMY_DATABASE_URI']`.

## Models

### Cafe

The `Cafe` model has the following fields:
- `id`: Integer, primary key
- `name`: String, unique, not null
- `map_url`: String, not null
- `img_url`: String, not null
- `location`: String, not null
- `seats`: String, not null
- `has_toilet`: Boolean, not null
- `has_wifi`: Boolean, not null
- `has_sockets`: Boolean, not null
- `can_take_calls`: Boolean, not null
- `coffee_price`: String

## Routes

### Home

- **`GET /`**: Render the homepage.

### Get a Random Cafe

- **`GET /random`**: Retrieve a random cafe from the database.

### Get All Cafes

- **`GET /all`**: Retrieve a list of all cafes.

### Search Cafes by Location

- **`GET /search`**: Search for cafes by location. Pass the location as a query parameter `loc`.

### Add a New Cafe

- **`POST /add`**: Add a new cafe to the database. Requires `api-key` as a query parameter.

### Update Cafe Price

- **`PATCH /update-price/<int:cafe_id>`**: Update the coffee price of a specific cafe. Pass the new price as a query parameter `new_price`.

### Delete a Cafe

- **`DELETE /report-closed/<int:cafe_id>`**: Delete a cafe from the database. Requires `api-key` as a query parameter.
