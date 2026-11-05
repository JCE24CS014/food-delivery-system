# Food Delivery System — Test Cases

These are **planned test cases** derived from the scope and user stories in [`STORYBOARD.md`](STORYBOARD.md). They are not execution results. Run them against the implemented system and record actual results before marking them passed.

## Preconditions and test data

- A test customer account, restaurant account, and delivery-partner account are available where needed.
- The restaurant has at least one available menu item and one unavailable item.
- Expected prices, delivery fee, and applicable tax rules are configured for the test environment.
- Use non-production test data; do not use real payment details.

## Functional test cases

| ID | Feature | Steps | Expected result | Priority |
|---|---|---|---|---:|
| TC-01 | Customer registration | Submit registration with valid required details. | Account is created once and the customer receives confirmation or is signed in, according to the design. | High |
| TC-02 | Registration validation | Submit registration with a missing required field or malformed email. | Registration is rejected with a clear validation message; no invalid account is created. | High |
| TC-03 | Sign in | Sign in with valid customer credentials. | Customer is authenticated and can access customer features. | High |
| TC-04 | Invalid sign in | Sign in with an incorrect password. | Access is denied and a non-revealing error is shown. | High |
| TC-05 | Browse restaurants | Open the restaurant listing. | Available restaurants and relevant details are displayed. | High |
| TC-06 | View menu | Select a restaurant. | Menu items, descriptions, prices, and availability are displayed. | High |
| TC-07 | Add item to cart | Add an available menu item to the cart. | Item and correct price appear in the cart. | High |
| TC-08 | Update quantity | Increase and decrease an item's quantity in the cart. | Quantity and subtotal update correctly; quantity cannot be less than one (or item removal is offered). | High |
| TC-09 | Remove item | Remove an item from the cart. | Item is removed and totals are recalculated correctly. | Medium |
| TC-10 | Unavailable menu item | Attempt to add an unavailable item to the cart. | Item cannot be ordered and the customer receives an availability message. | High |
| TC-11 | Cart total | Add multiple items and review the cart. | Item subtotals, fees, taxes (if configured), and final total follow the configured calculation rules. | High |
| TC-12 | Checkout validation | Attempt checkout with an empty cart or missing delivery address. | Order is not submitted; the missing information is identified. | High |
| TC-13 | Place order | Submit checkout with a non-empty cart and valid delivery address. | Exactly one order is created with the correct items, quantities, total, address, and initial status; an order reference is shown. | High |
| TC-14 | Restaurant accepts order | Sign in as restaurant staff and accept a pending order. | Order status changes to accepted and the customer can see the updated status. | High |
| TC-15 | Restaurant rejects order | Reject a pending order with a reason if required by the design. | Order status changes to rejected; the customer sees the outcome and the order is not sent for delivery. | High |
| TC-16 | Invalid order status transition | Attempt a transition that is not permitted by the defined lifecycle. | Update is rejected and the existing status remains unchanged. | High |
| TC-17 | Preparation status | Mark an accepted order as preparing and then ready for pickup. | Each permitted status is saved and visible to the customer. | Medium |
| TC-18 | Delivery assignment visibility | Sign in as a delivery partner and view assigned work. | The partner can see assigned deliveries and required delivery details, but not unassigned orders. | High |
| TC-19 | Delivery progress | Update an assigned order through picked-up and delivered statuses. | Permitted changes are recorded and the customer sees the latest status. | High |
| TC-20 | Customer order history | View order history as a signed-in customer. | The customer sees their own orders and statuses. | Medium |
| TC-21 | Order privacy | Try to view another customer's order while signed in as a different customer. | Access is denied and no other customer's order details are disclosed. | High |
| TC-22 | Feedback eligibility | Submit feedback for an order that is delivered, then try for a pending order. | Feedback for the delivered order is accepted; feedback for a non-delivered order is rejected. | Low |
| TC-23 | Duplicate order submission | Submit checkout once, then retry the same request or double-click submit. | The system does not create unintended duplicate orders; the customer sees a stable result. | High |
| TC-24 | Session and role access | Attempt restaurant or delivery-partner actions as a customer. | Unauthorized actions are denied; only permitted role actions are available. | High |

## Non-functional checks

| ID | Check | Expected result |
|---|---|---|
| NTC-01 | Input handling | Invalid or unexpected input is validated safely and does not crash the application. |
| NTC-02 | Authorization | Order and account data are accessible only to appropriately authorized users. |
| NTC-03 | Usability | Validation and order-status messages are understandable and identify the next action where possible. |
| NTC-04 | Reliability | Refreshing or revisiting an order does not silently change its saved contents or status. |
| NTC-05 | Responsive layout | Core browse, cart, and order-tracking flows remain usable on supported mobile and desktop screen sizes. |

## Execution record

No test execution has been recorded yet. Update this table after the application is implemented and tests are run.

| Run date | Environment / build | Passed | Failed | Not run | Notes |
|---|---|---:|---:|---:|---|
| Pending | Not available | — | — | All | Implementation and test environment not yet verified. |
