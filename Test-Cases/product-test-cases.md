# Product API Test Cases

## TC-001: Retrieve All Products

- **Module:** Products
- **Priority:** High
- **Type:** Positive
- **Method:** GET
- **Endpoint:** /products
- **Expected Result:** API returns HTTP 200
  and a list of products containing valid IDs
  and prices.
- **Actual Result:** HTTP 200, 30 products returned.
- **Status:** PASS

## TC-002: Retrieve Single Product

- **Module:** Products
- **Priority:** High
- **Type:** Positive
- **Method:** GET
- **Endpoint:** /products/1
- **Expected Result:** API returns HTTP 200
  and the requested product information.
- **Actual Result:** HTTP 200, product ID 1
  returned with the expected title and price.
- **Status:** PASS

## TC-004: Retrieve Nonexistent Product

- **Module:** Products
- **Priority:** Medium
- **Type:** Negative
- **Method:** GET
- **Endpoint:** /products/99999
- **Expected Result:** API returns an appropriate
  error response without returning a valid product.
- **Actual Result:** HTTP 404 with an error message.
- **Status:** PASS

## TC-003: Retrieve Product Using Invalid ID

- **Module:** Products
- **Priority:** Medium
- **Type:** Negative
- **Method:** GET
- **Endpoint:** /products/abc
- **Expected Result:** API returns an appropriate
  error response without returning a valid product.
- **Actual Result:** HTTP 404 with error message
  "Product with id 'abc' not found".
- **Status:** PASS

## TC-005: Search Products by Keyword

- **Module:** Product Search
- **Priority:** High
- **Type:** Positive
- **Method:** GET
- **Endpoint:** /products/search?q=phone
- **Expected Result:** API returns HTTP 200
  and a list of products relevant to the search keyword.
- **Actual Result:** HTTP 200, 23 products returned.
  All returned products had IDs and matched the search term.
- **Status:** PASS

## TC-006: Retrieve Products with a Limit

- **Module:** Products
- **Priority:** Medium
- **Type:** Positive
- **Method:** GET
- **Endpoint:** /products?limit=10
- **Expected Result:** API returns HTTP 200
  and no more than 10 products.
- **Actual Result:** HTTP 200, 10 products returned,
  limit is 10, and total is 194.
- **Status:** PASS

## TC-007: Retrieve Products with a Zero Limit

- **Module:** Products
- **Priority:** Medium
- **Type:** Boundary Value
- **Method:** GET
- **Endpoint:** /products?limit=0
- **Expected Result:** The API should handle a
  zero limit consistently and return an appropriate
  response.
- **Actual Result:** HTTP 200, all 194 products
  returned. The reported limit and total were both 194.
- **Status:** PASS (Observed behavior)

## TC-008: Retrieve Product Categories

- **Module:** Products
- **Priority:** Medium
- **Type:** Positive
- **Method:** GET
- **Endpoint:** /products/categories
- **Expected Result:** API returns HTTP 200
  and a non-empty list of categories with names.
- **Actual Result:** HTTP 200, 24 categories returned.
  All categories contained names.
- **Status:** PASS

## TC-009: Retrieve Products by Category

- **Module:** Products
- **Priority:** High
- **Type:** Positive
- **Method:** GET
- **Endpoint:** /products/category/smartphones
- **Expected Result:** API returns HTTP 200
  and only products belonging to the requested category.
- **Actual Result:** HTTP 200, 16 products returned.
  All returned products belonged to the smartphones category.
- **Status:** PASS

## TC-010: Retrieve Products from Invalid Category

- **Module:** Products
- **Priority:** Medium
- **Type:** Negative
- **Method:** GET
- **Endpoint:** /products/category/not-a-real-category
- **Expected Result:** API returns an empty products array
  when the requested category does not exist.
- **Actual Result:** HTTP 200, empty products array returned.
  No error message was provided.
- **Status:** PASS
