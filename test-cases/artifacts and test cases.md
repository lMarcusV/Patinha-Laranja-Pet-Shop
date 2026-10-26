# Artifacts, Test scenarios and

## 1. Artifacts

In software development, ensuring product quality is essential, and one of the key practices for this is software testing. To carry out tests efficiently, a set of test artifacts is used, which are documents, tools, and results that help plan, track, execute, and evaluate tests. These artifacts play a crucial role in organizing and running the testing process, making sure that all aspects are properly covered.

## 1.1 Recommended QA Artifacts

### 1.1.1 Test Strategy

Defines how quality will be validated: scope, objectives, risks, techniques, tools, priorities, and entry and exit criteria.

### 1.1.2 Test Plan

Organizes the modules to be tested, environments, types of tests, responsible people, and conditions to consider the application approved.

### 1.1.3 Test Cases and Checklist

Include ID, requirement, pre-conditions, steps, input data, expected result, actual result, and status.

### 1.1.4 Defect Report

Documents the issues found, with steps to reproduce, evidence, expected result, actual result, severity, and priority.

### 1.1.5 Execution and Closure Report

Summarizes executed tests, passed, failed, blocked, defects found, coverage, and remaining risks.

## 1.2 Complementary artifacts that add value

| Artifact	| What it's for |
| --- | --- |
| Traceability matrix	| Links requirements, scenarios, test cases, and defects. |
| Risk matrix	| Prioritizes tests based on failure probability and impact. |
| Test data	| Defines products, ZIP codes, boundary values, stocks, and invalid conditions. |
| Execution evidence	| Records screenshots, logs, and automation results. |
| Accessibility report	| Logs barriers found and checks performed. |

## 2 Test Cases

Test cases are essential documents for planning the tests to be carried out on software. They describe exactly the expected behavior of the software in certain situations, allowing us to understand if the features are working as intended. Test cases outline the actions that need to be taken to ensure the software behaves correctly and responds properly.
A QA works preventively, they don't wait for the application to be ready to test; they work by finding possible inconsistencies and flaws throughout the entire development cycle.  

## 2.1 Test Scenarios and Their Results

| ID	| Test Scenario	| Expected Result	| Priority |
| --- | --- | --- | --- |
| CT-001  | Access the application and open the catalog	| Page loads correctly and 16 products displayed	| High |
| CT-002  | Validate interface elements	| Fields, buttons, labels, and components are present and usable	| High |
| CT-003  | Check products on sale	| Four products identified as on sale	| Medium |
| CT-004  | Check product with no stock	| Purchase prevented and proper message displayed	| Critical |
| CT-005  | Add product to cart	| Item added correctly and subtotal calculated	| High |
| CT-006  | Change the quantity of an item in the cart	| Quantity and subtotal correctly updated, if the feature exists	| Medium |
| CT-007  | Remove an item from the cart	| Item removed and subtotal recalculated correctly	| Medium |
| CT-008  | Refresh the page with the cart filled	| Cart retrieved according to implemented persistence	| High |
| CT-009  | Validate required fields at checkout	| Submission prevented when required fields are empty	| High |
| CT-010  | Validate checkout data	| Valid data accepted and invalid data rejected according to defined rules	| High |
| CT-011  | Validate ZIP code format	| Invalid format rejected; valid format accepted without assuming the address exists	| Medium |
| CT-012  | Validate name field with legitimate names	| Legitimate names accepted, including spaces and accented characters	| High | 
| CT-013  | Purchase with a subtotal of R$ 249.99	| Shipping charged according to the business rule	| High |
| CT-014  | Purchase with a subtotal of R$ 250.00	| Free shipping applied	| High |
| CT-015  | Validate price filter boundaries	| Products correctly included or excluded at minimum and maximum limits	| Medium |
| CT-016  | Filter products by available criteria	| Only products matching the applied filters are displayed	| Medium |
| CT-017  | Confirm valid checkout	| Order registered with correct data and items	| Critical |
| CT-018  | Click confirmation button repeatedly	| Only one order created for the same confirmation	| Critical |
| CT-019  | Change or deplete stock before confirmation | Stock revalidated and purchase blocked when insufficient | Critical |
| CT-020  | Validate stock after completing the purchase | Stock updated correctly after the order is finalized | Critical |
| CT-021  | Add to cart in one tab and update in another | Cart state and button availability remain consistent or are updated correctly | High |
| CT-022  | Simulate localStorage failure | Application handles the failure, maintains memory operation when expected, and informs about the limitation | High |
| CT-023  | Validate consistency between provided and recorded data | Displayed, persisted, and order-associated data match the provided information | Critical |
| CT-024  | Check stored data | Only the data specified in the requirements are persisted | High |
| CT-025  | Restart the demo | Initial state restored according to the defined behavior | Medium |
| CT-026  | Check order list and details	| Order data matches the purchase made	| High |
| CT-027  | Validate success, error, and validation messages	| Correct, understandable messages displayed in the right context	| Medium |
| CT-028  | Validate exception handling	| Unexpected inputs and failures are handled without breaking the application |	High |
| CT-029  | Validate responsiveness on mobile devices	| Readable content, usable controls, and no major layout issues |	High |
| CT-030  | Navigate using only the keyboard	| Controls accessible via keyboard with noticeable visual focus |	High |
| CT-031  | Review interface texts and content |	No significant writing errors or unwanted visible source code	| Medium |
| CT-032  | Add items until reaching stock limit	| Quantities and availability are consistent; no purchases above allowed stock | High |
| CT-033  | Validate consistency after persistence failure |	Orders and stock remain consistent even when saving data fails | Critical |
| CT-034  | Perform regression on main flows	| Previously validated features continue working after changes or fixes	| High |
| CT-035  | Check that data is combined | Data entered in the freight ZIP code field does not sync with the delivery field	| Critical |
| CT-036  | Data entry fields | Change of data entry field according to payment method change | High |

