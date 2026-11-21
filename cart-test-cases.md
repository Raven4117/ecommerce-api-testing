# Shopping Cart API Test Cases

## TC-011: Retrieve All Shopping Carts

- **Module:** Shopping Cart
- **Priority:** High
- **Type:** Positive
- **Method:** GET
- **Endpoint:** /carts
- **Expected Result:** API returns HTTP 200
  and a list of shopping carts containing IDs,
  user IDs, and product arrays.
- **Actual Result:** HTTP 200, 30 carts returned
  out of 208 total. Cart objects contained the
  expected fields.
- **Status:** PASS

## TC-012: Retrieve Single Cart

- **Module:** Shopping Cart
- **Priority:** High
- **Type:** Positive
- **Method:** GET
- **Endpoint:** /carts/1
- **Expected Result:** API returns HTTP 200
  and the requested cart with its ID, user ID,
  and product details.
- **Actual Result:** HTTP 200, cart ID 1 returned,
  belonging to user ID 1. Cart contained 4 products
  with the expected product fields.
- **Status:** PASS

## TC-013: Retrieve Nonexistent Cart

- **Module:** Shopping Cart
- **Priority:** Medium
- **Type:** Negative
- **Method:** GET
- **Endpoint:** /carts/99999
- **Expected Result:** API returns HTTP 404
  with an appropriate error message and no cart data.
- **Actual Result:** HTTP 404 with message
  "Cart with id '99999' not found".
  No cart ID or products array was returned.
- **Status:** PASS

## TC-014: Create Shopping Cart

- **Module:** Shopping Cart
- **Priority:** High
- **Type:** Positive
- **Method:** POST
- **Endpoint:** /carts/add
- **Expected Result:** API returns a successful response containing a newly created cart with the requested user ID, products, and quantities.
- **Actual Result:** HTTP 201 Created, cart ID 209 returned for user ID 1. Two products were included: product ID 1 with quantity 2 and product ID 2 with quantity 1. Total products: 2. Total quantity: 3.
- **Status:** PASS


## TC-015: Update Existing Shopping Cart

- **Module:** Shopping Cart
- **Priority:** High
- **Type:** Positive
- **Method:** PUT
- **Endpoint:** /carts/1
- **Expected Result:** API returns HTTP 200 and an updated cart containing the requested product IDs and quantities.
- **Actual Result:** HTTP 200, cart ID 1 returned for user ID 1. Two products were included: product ID 1 with quantity 5 and product ID 2 with quantity 2. Total quantity: 7.
- **Status:** PASS

## TC-016: Delete Existing Shopping Cart

- **Module:** Shopping Cart
- **Priority:** High
- **Type:** Positive
- **Method:** DELETE
- **Endpoint:** /carts/1
- **Expected Result:** API returns HTTP 200 and confirms that the requested cart has been deleted.
- **Actual Result:** HTTP 200, cart ID 1 returned for user ID 1. Response included the isDeleted and deletedOn fields.
- **Status:** PASS
