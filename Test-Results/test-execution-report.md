
# Test Execution Report

## 1. Project Information

- **Project:** E-commerce API Testing
- **API:** DummyJSON
- **Testing Tool:** Postman
- **Scripting Language:** JavaScript
- **Test Environment:** https://dummyjson.com
- **Testing Type:** API Functional Testing

## 2. Test Execution Overview

This report summarizes the execution of API test cases
for the Products and Shopping Cart modules.

Testing included positive, negative, and boundary-value
scenarios. Automated assertions were implemented using
Postman's Post-response scripts.

The purpose of testing was to verify API responses,
HTTP status codes, response structures, and data accuracy.

## 3. Execution Summary

| Metric | Result |
|---|---:|
| Total Test Cases | 16 |
| Passed | 16 |
| Failed | 0 |
| Blocked | 0 |
| Not Executed | 0 |
| Pass Rate | 100% |

## 4. Test Coverage

| Module | Test Cases | Coverage |
|---|---|---|
| Products | TC-001 to TC-010 | Retrieval, search, filtering, invalid IDs, categories, boundary values |
| Shopping Cart | TC-011 to TC-016 | Retrieval, creation, updating, deletion, invalid IDs |

### HTTP Methods Tested

- GET
- POST
- PUT
- DELETE

### Testing Scenarios

- Positive testing
- Negative testing
- Boundary-value testing
- Response validation
- HTTP status code validation

## 5. Observations and Limitations

### Observations

- The `/products?limit=0` endpoint returned all 194 available products instead of an empty result.
- Searching for a nonexistent product category returned HTTP 200 with an empty products array.
- Invalid product and cart IDs returned HTTP 404 with appropriate error messages.
- The cart creation, update, and deletion endpoints returned successful responses with the expected data.

### API Limitations

- DummyJSON simulates POST, PUT, and DELETE operations. Changes are not permanently persisted in its database.
- API responses therefore demonstrate the expected operation results but do not confirm permanent database changes.
- This project focuses on API response validation and does not test a real e-commerce backend or database.

## 6. Defect Summary

No confirmed defects were identified during the execution
of the 16 documented test cases.

Several observations were recorded, including the behavior
of the products endpoint when using a limit of zero.
However, no formal API specification was available to
determine whether this behavior represents a defect.

A reusable bug report template was created for documenting
potential defects in future testing activities.

## 7. Conclusion

All 16 documented test cases were recorded as passed.

The Products and Shopping Cart API endpoints returned
responses matching the expected results defined for
the executed test scenarios.

Postman automated assertions were used to validate
HTTP status codes, response structures, product data,
cart information, and deletion indicators.

The project provided practical experience with API
functional testing, negative testing, boundary-value
testing, JavaScript assertions, and test documentation.

Testing was performed using DummyJSON, which simulates
data modification operations rather than permanently
storing changes.




