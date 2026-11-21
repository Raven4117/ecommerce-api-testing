
# Test Plan — E-commerce API Testing

## 1. Introduction

This project focuses on functional API testing of
the Products and Shopping Cart endpoints provided
by DummyJSON.

The goal is to verify API responses, data accuracy,
HTTP status codes, and response structures.

## 2. Testing Objectives

- Verify successful API requests.
- Validate HTTP status codes.
- Verify JSON response structures.
- Validate product and shopping cart data.
- Test invalid IDs and categories.
- Perform boundary-value testing.
- Implement automated assertions using JavaScript.

## 3. Scope of Testing

### In Scope

- Products API
- Product Search API
- Shopping Cart API
- GET, POST, PUT, and DELETE requests
- Positive testing
- Negative testing
- Boundary-value testing
- Response validation

### Out of Scope

- User interface testing
- Performance and load testing
- Security testing
- Database persistence verification
- Real payment processing

## 4. Testing Tools

| Tool | Purpose |
|---|---|
| Postman | API request execution and validation |
| JavaScript | Automated assertions |
| DummyJSON | Simulated REST API |
| Visual Studio Code | Test documentation and project files |
| Git and GitHub | Version control and project hosting |

## 5. Test Approach

Testing was performed manually through Postman
requests, with automated assertions implemented
using Postman Post-response scripts.

Each test case was executed against the relevant
API endpoint. Actual responses were compared
against expected results.

## 6. Entry Criteria

- API endpoint is accessible.
- Postman is installed and configured.
- Test cases have been documented.
- Required request configurations are prepared.

## 7. Exit Criteria

- All planned test cases have been executed.
- Test results have been documented.
- Automated assertions have been reviewed.
- Test execution report has been completed.

## 8. Test Environment

- API: https://dummyjson.com
- Tool: Postman
- Scripting Language: JavaScript
- Operating System: Windows

## 9. Risks and Limitations

DummyJSON simulates data modification operations.
POST, PUT, and DELETE responses do not permanently
modify the database.

Testing therefore validates API responses rather
than permanent changes to stored data.

## 10. Deliverables

- Test Plan
- Test Cases
- Postman Collection
- Test Execution Report
- Bug Report Template
- Project README
