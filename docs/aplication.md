# Patinha Laranja Pet Shop - Web Aplication

Aplication: https://lmarcusv.github.io/Patinha-Laranja-Pet-Shop-App/

## Application, techniques and their use

## 1. About the aplication

Patinha Laranja is a demo online store for pet products, designed to showcase a simple and welcoming online shopping experience. 

The application features a product catalog, search and category filters, product details, quantity controls, and a shopping cart. Customers can enter delivery details, choose a simulated payment method, review their order, and view their order history. 

The app also includes features for checking product availability and stock, as well as resetting the demo data.

With a responsive design, accessible navigation, and clear information at every step, the application offers a functional showcase of the shopping journey in a virtual pet shop. All orders and payments are simulated: no actual charges are made, and no products are shipped.

## 2. Techniques used

The goal is not just to check if the store works, but also to identify defects that could compromise a purchase, generate duplicate orders, show incorrect amounts, or leave the application's state inconsistent.

### 2.1 Recommended testing techniques

#### 2.1.1 Functional Testing — Black Box

Critical Priority

Validate features through the interface, without needing to know the internal implementation.

- Open the catalog with 16 products.
- Filter, search, and sort products.
- View details of a product.
- Add, remove, and change quantities in the cart.
- Calculate subtotal, shipping, and total.
- Complete a purchase with Pix, boleto, or a simulated card.
- Check completed orders and their details.

Techniques: equivalence partitioning, boundary value analysis, and decision tables.

#### 2.1.2 Integration tests between modules

Check if the catalog, cart, inventory, checkout, orders, and persistence operations maintain the same data and rules.

Example: add two products, update the quantity, complete the purchase, and check if the cart was emptied, the inventory was reduced, and the order was properly registered.

#### 2.1.3 Persistence and recovery tests

- Refresh the page and check if the cart is recovered.
- Close and reopen the browser.
- Test missing, corrupted, or incompatible data in `localStorage`.
- Simulate unavailable storage or a write failure.
- Restart the demo and check if the initial state was restored.

Technique: state and state-transition testing.

#### 2.1.4. Negative and security tests

- Try to confirm an order without any items.
- Try to purchase a product that’s out of stock.
- Change the quantity to zero, negative, or an excessive value.
- Modify the stock from the browser console.
- Try to confirm the order repeatedly and quickly.
- Enter unexpected text in personal information fields.

Check validation, error messages, and data consistency. Since the rules run on the client side, tests should also document the security limits of this architecture.

#### 2.1.5. Interface, responsiveness, and accessibility tests

Validate desktop and mobile versions, keyboard navigation, visible focus, field labels, validation messages, contrast, zoom, and reading with assistive technologies.

#### 2.1.6. Regression and Exploratory Testing

Rerun the main flows after each change and explore unexpected combinations, like going back from checkout to the cart, refreshing the page during navigation, or resetting the data with an already registered order.

#### 2.1.7 Integration Testing

Validate that the data entered or provided is communicating with other data. In these tests, the data should be combined, preventing the entry of data that don't complement each other.

## 3. Applying the Techniques to Store Requirements

This is the most important part of planning: turning each business rule into clear test scenarios.

### 3.1 Equivalence Partitioning and Boundary Value Analysis

These techniques help you pick test cases without having to test every possibility.

Example 1 — Free shipping for orders over R$ 250.00

| **Purchase Amount**	| **Expected Result** |
| --- | --- |
| R$ 249.99	| Shipping paid |
| R$ 250.00 |	Free shipping |
| R$ 250.01 |	Free shipping |

Example 2 — Inventory

| Condition	| Expected Result |
| --- | --- |
| Product with available stock	| Allow adding to cart |
| Product with stock equal to zero	| Prevent purchase |
| Requested quantity equal to stock	| Allow if all other rules are met |
| Requested quantity greater than stock	| Prevent or adjust the quantity according to the defined rule |

Example 3 — ZIP Code

The calculation considers the first digit of the ZIP code. Test all ten possible digits, from 0 to 9, checking the corresponding shipping range.

Also, test empty ZIP codes, incomplete ones, those with letters, and those with special characters. The format validation rule needs to be defined in the requirement or confirmed with the person who developed the application.

### 3.2 Decision Tables

Use this technique when the outcome depends on more than one condition.

Example: confirming an order.

| Cart	| Stock |	Required data	| Result |
| --- | --- | --- | --- |
| Empty |	—	| —	| Block |
| With items	| Available	| Valid	| Confirm |
| With items	| Insufficient	| Valid	| Block |
| With items	| Available	| Invalid	| Block |
| With items	| Available	| Valid, but repeated confirmation	| Create only one order |

This table helps you avoid testing only the "happy path".
