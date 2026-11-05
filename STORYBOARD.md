# Food Delivery System — Storyboard and Progress

## Project problem

**Selected problem:** Food delivery system.

Customers often need a convenient way to discover nearby restaurants, browse menus, place orders, and follow delivery progress. Restaurants need a clear way to receive and manage orders, while delivery partners need the order and delivery information required to complete deliveries. This project will describe and plan a system connecting these participants and supporting the order lifecycle.

## Project goal

Plan a simple food delivery application that lets a customer register or sign in, browse restaurants and menu items, build a cart, place an order, and track its status. Restaurant staff can accept or reject orders and update preparation status. A delivery partner can view an assigned delivery and update delivery progress.

## Users and needs

- **Customer:** Find food, place an order, pay or choose an available payment method, and know the order status.
- **Restaurant staff:** Review incoming orders and update acceptance and preparation status.
- **Delivery partner:** See assigned delivery details and report pickup and delivery progress.
- **Administrator (future/optional):** Manage accounts, restaurants, and operational issues.

## Storyboard

1. **Discover:** The customer opens the application and browses restaurants and menus.
2. **Choose:** The customer selects available menu items and adds them to a cart.
3. **Review:** The customer checks quantities, prices, delivery address, and total before ordering.
4. **Place order:** The customer submits the order and receives an order reference and initial status.
5. **Prepare:** Restaurant staff review the order, accept or reject it, and update preparation progress.
6. **Deliver:** A delivery partner receives the assignment, picks up the order, and updates its delivery status.
7. **Complete:** The customer sees the delivered status and can optionally provide feedback.

## User stories and progress board

Progress reflects the state of this repository when this planning document was created. **No application implementation has been verified yet.**

| ID | User story | Priority | Status | Acceptance summary |
|---|---|---:|---|---|
| US-01 | As a customer, I want to create an account and sign in so that I can place and view my orders. | High | Planned | Valid details create/sign in to an account; invalid details show a helpful error. |
| US-02 | As a customer, I want to browse restaurants and menus so that I can choose food. | High | Planned | Restaurant and menu details are visible; unavailable items cannot be ordered. |
| US-03 | As a customer, I want to manage a cart so that I can review items and quantities before checkout. | High | Planned | Add, remove, and quantity changes update the cart and total correctly. |
| US-04 | As a customer, I want to submit an order with a delivery address so that the restaurant can prepare it. | High | Planned | A valid non-empty cart and address produce an order with an initial status. |
| US-05 | As restaurant staff, I want to accept or reject an incoming order so that the customer receives a decision. | High | Planned | Only valid status changes are accepted and made visible to the customer. |
| US-06 | As restaurant staff, I want to update preparation status so that the customer knows the order progress. | Medium | Planned | Status changes follow the defined order lifecycle. |
| US-07 | As a delivery partner, I want to view assigned deliveries and update their progress so that the customer can track delivery. | Medium | Planned | Assigned order details are available and delivery status updates are recorded. |
| US-08 | As a customer, I want to view order status and order history so that I can track current and past orders. | Medium | Planned | Customers can access only their own order information. |
| US-09 | As a customer, I want to submit feedback after delivery so that I can share my experience. | Low | Planned | Feedback is accepted only for an order belonging to the customer that is delivered. |

## Progress summary

- **Problem selected and documented:** Complete.
- **Initial user roles, goal, storyboard, and backlog:** Complete.
- **Application design and implementation:** Not started / not verified in this repository.
- **Test plan:** Drafted in [`TEST_CASES.md`](TEST_CASES.md); execution is pending implementation.

## Suggested milestones

1. **Planning:** Confirm requirements, roles, storyboard, and acceptance criteria. *(Planning documents drafted.)*
2. **Core customer flow:** Implement account access, restaurant/menu browsing, cart, and checkout.
3. **Order operations:** Implement restaurant order handling and order status updates.
4. **Delivery and tracking:** Implement delivery assignment, delivery progress, and customer tracking.
5. **Verification:** Run and record the test cases, fix defects, and review security and usability.

## Assumptions and scope notes

- This is a requirements and planning document; it does not claim these features have already been built.
- Payment processing, live maps, notifications, refunds, and administrator tools are future scope unless added to the project requirements.
- The implementation should enforce role-based access and protect customer and order information.
- The exact technology stack and payment options have not yet been specified.
