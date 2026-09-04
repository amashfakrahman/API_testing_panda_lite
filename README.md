# Panda Lite API Collection

A Postman API collection for testing the Panda Lite food delivery platform APIs.

This collection contains API requests for authentication, restaurant management, order processing, health checking, and database inspection.

## Overview

Panda Lite is a food delivery system that supports different types of users:

- Customer
- Restaurant
- Rider

The API collection helps developers and testers verify the complete application workflow, starting from user registration and login to restaurant operations and order delivery.

## Features

### Authentication

The authentication module includes:

- Customer registration
- Restaurant registration
- Rider registration
- User login
- Input validation testing

Available endpoints:

POST /auth/register
POST /auth/login

The API uses the following header for authentication:

X-STQA-Key

## Restaurant Management

Restaurant-related API operations include:

- Create restaurant
- Add menu items
- Manage restaurant actions
- Handle customer orders

Example endpoint:

POST /restaurants

## Order Management Workflow

The collection covers the complete order process:

1. Customer places an order
2. Restaurant accepts the order
3. Restaurant starts preparing the order
4. Restaurant marks the order as ready
5. Rider claims the order
6. Rider picks up the order
7. Rider delivers the order
8. Customer rates the order

## Health Check

The API includes a health check endpoint to verify server availability.

GET /_internal/health

## Database Inspection

The collection provides an endpoint to inspect the current database state.

GET /_internal/db-state

It can be used to check:

- Users
- Restaurants
- Menu items
- Orders
- Ratings

## Environment Variables

Configure these variables in Postman:

| Variable | Description |
|----------|-------------|
| BASE_URL | API base URL |
| STQA_KEY | API security key |
| CUSTOMER_TOKEN | Customer authentication token |
| RIDER_TOKEN | Rider authentication token |
| RESTAURANT_USER_ID | Restaurant user ID |
| ORDER_ID | Order ID |
| MENU_ITEM_ID | Menu item ID |

## How to Use

1. Import Panda Lite Collection.json into Postman.
2. Configure BASE_URL and STQA_KEY.
3. Run individual requests or the complete collection using Postman Collection Runner.

## Testing

The collection includes Postman test scripts to verify:

- Response status codes
- Successful API operations
- Generated IDs
- Authentication responses

## Technologies Used

- REST API
- Postman Collection
- JSON
- Bearer Authentication
- API Testing

## License

This project is intended for development and testing purposes.
