# PROMPT — CREATION OF AN ONLINE PET SHOP E-COMMERCE WEB APPLICATION USING GENERATIVE AI

## 1. Role of AI

Act as a senior web developer, specializing in HTML5, CSS3, JavaScript, UX/UI, responsiveness, accessibility, and e-commerce business rules.

Your goal is to create a functional, well-organized, and visually professional e-commerce web application using only technologies that run in the browser.

**MANDATORY RESTRICTION: DO NOT CREATE AUTOMATED TESTS.**

Do not generate test files, test scripts, unit tests, automated integration tests, end-to-end tests, test framework configurations, test pipelines, or dependencies meant for test automation.

Do not use tools or frameworks such as Jest, Vitest, Cypress, Playwright, Selenium, Mocha, or equivalents.

The subsequent validation of the application will be carried out manually by a Quality Assurance (QA) professional, using techniques, scenarios, test cases, and documented evidence outside the application's source code. 

## 2. Business Context
Create a fictitious online store called OrangeTech Store, specializing in selling electronics and tech accessories to end consumers (B2C). The target audience is people who want to research, compare, and buy tech products using computers, tablets, or smartphones. The goal is to provide a simple, intuitive, responsive, and consistent shopping experience. The application will be used as a demo project to practice manual software testing, risk analysis, defect identification, and quality documentation. 

## 3. Mandatory Technical Requirements
- Develop the application in a single file called index.html.
- Use HTML5 to structure the application.
- Put all the CSS inside a single style tag in the HTML itself.
- Put all the JavaScript inside one or more script tags in the same HTML.
- Do not create external CSS or JavaScript files.
- Do not use interface frameworks like React, Angular, or Vue.
- Do not require installation of dependencies, compilation, or an application server for the basic demo.
- Use localStorage to preserve non-sensitive data between sessions, like cart and preferences.
- Handle errors when reading and writing to local storage.
- Do not store passwords, financial data, or unnecessary personal information.
- The application should work on modern browsers and adapt to both desktop and mobile screens.
- Do not rely on external APIs for essential functionality.
- If you use external images, provide visual alternatives or placeholders for cases where images don’t load.
- Use fictitious product data and prices in reais (R$).

## 4. Visual Identity and User Experience 

Adopt a dark theme with orange tones as the accent color. 

Visual reference: 
- Main background: graphite or almost black.
- Cards and panels: dark gray.
- Accent color: orange.
- Main text: white or light gray.
- Secondary text: gray with enough contrast.
- Primary buttons: orange with readable text.
- Success, warning, and error states: distinct and accessible colors.

Use a modern layout, consistent spacing, legible typography, product cards, understandable icons, and visual feedback for user actions. 

Ensure keyboard navigation, visible focus, field labels, accessible validation messages, and proper contrast. 

## 5. Required Features 

### 5.1 Home Page 
- Header with OrangeTech Store logo.
- Search field.
- Navigation by categories.
- Access to the cart with item quantity indicator.
- Highlight area for products and offers.
- Catalog with fictitious products.

### 5.2 Product catalog 
- Display at least 12 fictitious products.
- Use categories like smartphones, laptops, audio, peripherals, and accessories.
- Show name, image or placeholder, price, category, and availability.
- Provide a button to add to the cart.
- Show out-of-stock indication when inventory is zero.

### 5.3 Search, filters, and sorting
- Search products by name.
- Filter by category.
- Filter by price range.
- Sort by lowest price, highest price, and name.
- Display an appropriate message when no products match the search.
- Allow clearing the filters.

### 5.4 Product details 
- Show full description.
- Show price and availability.
- Allow selecting quantity based on stock.
- Allow adding the product to the cart.
- Validate data and quantities before updating the cart.

### 5.5 Shopping cart 
- Add products.
- Remove products.
- Increase or decrease quantities.
- Prevent invalid quantities or quantities exceeding stock.
- Automatically update subtotal and total.
- Display the empty cart state.
- Preserve the cart after page refresh.
- Provide an option to empty the cart with confirmation.
- Avoid duplicate products as independent lines when they can be grouped by the same identifier.

### 5.6 Shipping 
- Provide a field for ZIP code.
- Validate the ZIP code format.
- Simulate shipping cost calculation with clearly defined local rules.
- Inform a fictitious estimated delivery time.
- Recalculate the total when the shipping method changes.
- Do not claim that the delivery time or amount represents a real quote.

### 5.7 Checkout and purchase completion 
- Show a summary of products, quantities, subtotal, shipping, and total.
- Request only the fictitious data necessary for the demonstration.
- Validate required fields, formats, and inconsistent data.
- Offer payment methods only as simulated options.
- Do not request or store real card numbers, security codes, or bank passwords.
- Present a review step before confirmation.
- Allow completing a simulated purchase.
- Generate a demonstrative order identifier.
- Display order confirmation with a purchase summary.
- Do not make real charges or financial integrations.
- Do not complete a purchase with an empty cart or insufficient stock.

### 5.8 Order history 
- Record fake orders in localStorage.
- Display simulated orders and their items.
- Allow viewing the details of an order.
- Handle the absence of history.
- Avoid duplicating the same order due to repeated clicks on confirmation.

### 5.9 Feedback and error handling 
- Display success, warning, and error messages.
- Prevent invalid actions.
- Offer loading states when it makes sense.
- Display understandable messages instead of showing technical errors directly to the user.
- Handle invalid data, unavailable storage, and absence of products.
- Ask for confirmation for destructive actions.

## 6. Business Rules
- Each product must have a unique identifier, name, category, price, description, image or placeholder, and stock.
- Prices and totals should be calculated consistently, preferably using integer values in cents to avoid monetary inaccuracies.
- The total should correspond to the subtotal plus shipping, considering the demonstrated rules.
- The quantity of each item must be a positive integer.
- Stock can never be exceeded by a valid operation.
- A simulated purchase should reduce the demonstration stock and update the persisted data.
- Changes in the cart should immediately update the interface.
- Invalid data in localStorage must not prevent the entire application from working.
- Confirmation messages should reflect the actual outcome of the operation.
- Persisted data should be treated as untrusted and validated before use.
- Do not simulate backend security: rules implemented only in the browser do not guarantee integrity against user manipulation.

## 7. Code architecture and organization 

Even if everything is in a single HTML file, organize the code clearly. 

Logically separate: 
- Data and product catalog.
- Current application state.
- Persistence functions.
- Interface rendering.
- Search, filters, and sorting.
- Cart operations.
- Subtotal, shipping, and total calculations.
- Form validation.
- Checkout and order creation.
- Messages and error handling.

Use clear variable and function names, avoid code duplication, and keep business rules separate from visual handling whenever possible. 

Do not use eval or execute code coming from user input. Avoid inserting untrusted inputs directly through innerHTML. 

## 8. Responsiveness 

The application should work on: 
- Desktop.
- Laptop.
- Tablet.
- Smartphone.

Use responsive CSS and media queries. 

On mobile: 
- Adjust the product grid.
- Avoid unnecessary horizontal scrolling.
- Keep buttons and fields easy to use by touch.
- Adapt navigation, cart, and checkout to screen width.
- Ensure content readability and accessibility.

## 9. Scope restrictions 

Do not implement: 
- Automated tests of any kind.
- Testing frameworks or test configuration files.
- Backend or remote database.
- Real authentication.
- Real payments.
- Mandatory integration with external services.
- Collection of unnecessary personal data.

Do not confuse a simulated purchase with a real commercial transaction. 

## 10. Expected delivery 

Deliver the full content of the index.html file, including HTML, CSS, and JavaScript.

The file must be able to be saved locally and opened in a modern browser. 

Before presenting the delivery: 
- Review the consistency between the implemented functionalities and the requirements.
- Check if all essential functionalities are connected to their respective interface controls.
- Review the business rules and error handling.
- Check the use of localStorage.
- Check the responsive behavior.
- Remove references to automated tests and unnecessary dependencies.
- Do not claim that the application has been run or validated in real browsers if that has not happened.

Do not create or run automated tests. Functional validation will be carried out manually later. 

First, present a brief description of the architecture and limitations of the solution. Then, deliver the complete code of the index.html file. 

Finally, provide a list of implemented functionalities and simple instructions to open the application locally.
