# Panda Lite API Testing Collection

## Overview

Panda Lite is a food delivery API system supporting Customer, Restaurant, and Rider roles. This Postman collection tests authentication, restaurant management, menu operations, order lifecycle, ratings, and internal diagnostic endpoints.

## Features Tested

### Authentication Module
- Customer registration
- Restaurant registration
- Rider registration
- Required field validation
- Password length validation
- Invalid role validation
- Invalid email validation
- Customer, Restaurant, and Rider login

### Restaurant & Menu Management
Tested endpoints:
- POST /restaurants
- POST /restaurants/{restaurantId}/menu
- PATCH /restaurants/{restaurantId}
- PATCH /menu-items/{menuItemId}

Coverage:
- Restaurant creation
- Duplicate restaurant validation
- Menu item creation
- Owner permission validation
- Negative price validation

### Order Lifecycle Testing

Workflow:
Customer places order → Restaurant accepts → Preparing → Ready for pickup → Rider claims → Pickup → Delivery

Test scenarios:
- Unauthorized order placement
- Invalid quantity handling
- Accept order
- Start preparing
- Mark ready for pickup
- Prevent duplicate claiming
- Pickup permission validation
- Delivery permission validation
- Order cancellation
- Cancellation fee validation

### Rating Testing
- Rating range validation (1-5)

### Internal Diagnostic Endpoints

- GET /_internal/health
- GET /_internal/db-state

## Environment Variables

| Variable | Description |
|---|---|
| BASE_URL | API base URL |
| STQA_KEY | API authentication key |
| CUSTOMER_ID | Customer ID |
| RESTAURANT_USER_ID | Restaurant user ID |
| CUSTOMER_TOKEN | Customer token |
| RESTAURANT_TOKEN | Restaurant token |
| RIDER_TOKEN | Rider token |
| ORDER_ID | Order ID |

## Test Execution

1. Open Postman
2. Import PandaLite_Collection.json
3. Configure environment variables
4. Run the collection
5. Review test results

## Test Coverage

The testing report includes:
- Test Plan
- Test Cases
- Defect Reports

Total documented test cases: 30

## Defect Summary

Identified defects include:
- Password length validation issue
- Invalid email acceptance
- Duplicate restaurant creation
- Negative price handling
- Unauthorized order access
- Invalid order quantity server error
- Data security issue
- Multiple order claiming issue
- Unauthorized pickup/delivery
- Cancellation fee issue
- Rating validation issue

## Conclusion

This collection provides API verification coverage for major Panda Lite workflows and can be used for regression testing, validation, and defect tracking.
