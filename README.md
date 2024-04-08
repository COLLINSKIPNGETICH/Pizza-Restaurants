# Pizza-Restaurants

This Flask application provides a simple API for managing pizza restaurants and their pizzas.

## Installation

1. Clone the repository:

## Create a virtual environment and install dependencies

python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
Set up the database:
flask db init
flask db migrate
flask db upgrade

## Run the application

flask run
Usage
Once the application is running, you can use a tool like Postman to interact with the API endpoints. The base URL for the API is <http://localhost:5000/>.

Endpoints
GET /restaurants: Get a list of all restaurants.
GET /restaurants Get details of a specific restaurant by ID.
DELETE /restaurants Delete a restaurant by ID.
GET /pizzas: Get a list of all pizzas.
POST /restaurant_pizzas: Create a new relationship between a restaurant and a pizza.
Models
Restaurant
id: Unique identifier for the restaurant.
name: Name of the restaurant (max length: 50).
address: Address of the restaurant.
Pizza
id: Unique identifier for the pizza.
name: Name of the pizza.
ingredients: Ingredients of the pizza.
RestaurantPizza
id: Unique identifier for the restaurant-pizza relationship.
price: Price of the pizza at the restaurant.
restaurant_id: ID of the restaurant.
pizza_id: ID of the pizza.
Validations
Restaurant name must be unique and less than 50 characters.
RestaurantPizza price must be between 1 and 30.
