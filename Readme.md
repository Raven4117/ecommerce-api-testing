
# E-commerce API Testing

## Project Overview

This project focuses on API functional testing of a simulated
e-commerce application using the DummyJSON API.

The purpose of the project was to practice API testing,
validate HTTP responses, verify response structures, and
identify unexpected API behavior using Postman.

## Tools and Technologies

- Postman
- JavaScript
- DummyJSON REST API
- Visual Studio Code
- Git and GitHub

## Project Scope

The project covers two API modules:

### Products

- Retrieve all products
- Retrieve a single product
- Search products
- Retrieve products with a specified limit
- Retrieve product categories
- Filter products by category
- Test invalid product IDs and categories
- Boundary-value testing

### Shopping Cart

- Retrieve all shopping carts
- Retrieve a single cart
- Test nonexistent cart IDs
- Create a shopping cart
- Update an existing shopping cart
- Delete a shopping cart

## Testing Approach

Testing included:

- Positive testing
- Negative testing
- Boundary-value testing
- HTTP status code validation
- Response body validation
- Automated assertions using JavaScript

Postman Post-response scripts were used to verify
API responses automatically.

## Test Results

- Total test cases: 16
- Passed: 16
- Failed: 0
- Pass rate: 100%

See `Test-Results/test-execution-report.md`
for the execution summary and observations.

## Project Structure

ecommerce-api-testing/
├── README.md
├── Test-Plan/
├── Test-Cases/
├── Postman/
├── Test-Results/
└── Bug-Reports/

## Important Notes

DummyJSON is a simulated API environment.
POST, PUT, and DELETE operations return simulated
responses and do not permanently modify the database.

The results demonstrate API response validation
rather than verification of persistent database changes.

## Learning Outcomes

Through this project, I gained practical experience with:

- REST API testing
- HTTP methods and status codes
- JSON response validation
- Postman automated testing
- JavaScript assertions
- Positive and negative test scenarios
- Boundary-value analysis
- Test case documentation
- Test execution reporting
