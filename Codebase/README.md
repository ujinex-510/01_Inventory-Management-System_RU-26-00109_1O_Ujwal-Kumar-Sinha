# Inventory Management System

## Project Overview
The **Inventory Management System** is a menu-driven, console-based Python application designed to track and manage product stock in real time. Built using core Python data structures—specifically a list of dictionaries—it stores each item with an auto-generated unique identifier (`I101` onward), item name, available quantity, and unit price. The system provides an interactive command-line loop that allows users to perform complete Create, Read, Update, and Delete (CRUD) operations, monitor low-stock thresholds, search records by ID, and calculate real-time financial stock valuations within an active session.

---

## Test Cases Documentation

### Test Case 1: Add Item (`Choice 1`)
* **Objective:** Verify that new items can be added to the inventory with auto-generated IDs and proper input validation.
* **Workflow:**
  * Prompts the user for the item name, quantity, and price.
  * Validates that neither the quantity nor the price is negative. If a negative value is entered, the system rejects the entry and displays an error message without incrementing the ID counter.
  * On valid input, assigns a sequential ID starting from `I101`, appends the item record to the inventory list, and displays a confirmation message.
  * Checks if the entered quantity is below `5`; if so, triggers an immediate low-stock warning.
  * Prompts the user to continue adding items in a loop until `"yes"` is no longer entered.

---

### Test Case 2: View Items (`Choice 2`)
* **Objective:** Verify that all stored inventory records are displayed accurately in a tabular format.
* **Workflow:**
  * Checks whether the inventory list contains any records.
  * If empty, notifies the user that the inventory has no items.
  * If populated, renders a formatted header (`ID`, `Name`, `Quantity`, `Price`) and iterates through every item in the list to display its current details.

---

### Test Case 3: Update Item (`Choice 3`)
* **Objective:** Verify that the quantity and price of an existing item can be modified using its unique ID.
* **Workflow:**
  * Prompts the user for the target Item ID and searches the inventory list for an exact match.
  * If found, prompts for the new quantity and new price, validating that neither value is negative before overwriting the existing record.
  * Displays a success message upon updating.
  * If the entered ID does not exist in the inventory, displays a "not found" error message.

---

### Test Case 4: Delete Item (`Choice 4`)
* **Objective:** Verify that an existing item can be permanently removed from the inventory using its Item ID.
* **Workflow:**
  * Prompts the user for the Item ID to delete and searches the inventory list.
  * If a matching ID is found, removes the item from the list, confirms the deletion by item name, and displays the updated count of remaining items.
  * If no matching ID is found, notifies the user that the item does not exist.

---

### Test Case 5: Total Stock Value (`Choice 5`)
* **Objective:** Verify that the system accurately calculates both individual item values and the overall inventory valuation.
* **Workflow:**
  * Checks if the inventory is empty; if so, displays an empty-inventory message.
  * Otherwise, iterates through each item, multiplies its quantity by its unit price to display the individual stock value, and accumulates the sum into a grand total displayed at the end.

---

### Test Case 6: Low Stock Report (`Choice 6`)
* **Objective:** Verify that the system filters and reports all items running low on stock.
* **Workflow:**
  * Scans the entire inventory for items whose quantity is strictly less than `5`.
  * Displays the ID, name, and current quantity of every matching item.
  * If all items have a quantity of `5` or more (or if the inventory is empty), informs the user that there are no low-stock items.

---

### Test Case 7: Search Item (`Choice 7`)
* **Objective:** Verify that a specific item can be retrieved and inspected using its Item ID.
* **Workflow:**
  * Prompts the user for an Item ID and scans the inventory list for a match.
  * If found, displays the complete record (`ID`, `Name`, `Quantity`, and `Price`).
  * If no record matches the entered ID, displays a "not found" message.

---

### Test Case 8: Exit & Invalid Menu Handling (`Choice 8` & Fallback)
* **Objective:** Verify clean program termination and graceful handling of invalid menu selections.
* **Workflow:**
  * Selecting `8` prints a closing message and breaks out of the main execution loop to terminate the program cleanly.
  * Entering any value outside `1` through `8` triggers the fallback condition, displaying an error prompt instructing the user to enter a valid menu number without crashing the application.