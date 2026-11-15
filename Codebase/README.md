# Inventory Management System

## Project Description

The Inventory Management System is a simple Python-based project used to manage items in an inventory.

It allows users to add, view, update, delete and search items. It also calculates the total stock value and displays items with low stock.

This project is developed using basic Python concepts such as lists, dictionaries, loops, conditional statements and exception handling.

## Features

1. **Add Item** - Add new items to the inventory.
2. **View Items** - Display all available items.
3. **Update Item** - Update the quantity and price of an item.
4. **Delete Item** - Remove an item using its unique ID.
5. **Total Stock Value** - Calculate the total value of all items.
6. **Low Stock Report** - Display items having a quantity below 5.
7. **Search Item** - Search for an item using its ID.
8. **Exit** - Close the program.

## Technologies Used

- Python 3
- Lists and dictionaries
- While and for loops
- If-else statements
- Try-except exception handling
- User input

## How to Run the Project

1. Install Python 3 on your computer.
2. Open the project folder in VS Code or a terminal.
3. Run the following command:

```bash
python inventory.py
```

## Item ID System

Every item receives a unique ID automatically:

- First item: `I101`
- Second item: `I102`
- Third item: `I103`

## Stock Management Rules

- Quantity cannot be negative.
- Price cannot be negative.
- Items with a quantity below 5 are considered low-stock items.
- Invalid item IDs are handled by the program.
- Stock value is calculated as:

  **Stock Value = Quantity × Price**

## Sample Test Case

| Item Name | Quantity | Price |
|---|---:|---:|
| Pen | 50 | 10 |
| Notebook | 3 | 40 |

Expected total stock value:

```text
Pen : 500.0
Notebook : 120.0
Total Stock Value: 620.0
```

Expected low-stock report:

```text
I102 | Notebook | Qty: 3
```

## Project Structure

```text
Inventory-Management-System/
├── inventory.py
└── README.md
```

## Learning Outcomes

Through this project, I learned:

- How to use lists and dictionaries in Python.
- How to perform basic CRUD operations.
- How to use loops and conditional statements.
- How to handle invalid user inputs.
- How to create a menu-driven Python program.
- How to manage inventory records.

## Conclusion

This project helped me understand the practical implementation of basic Python programming concepts by developing a simple Inventory Management System.
