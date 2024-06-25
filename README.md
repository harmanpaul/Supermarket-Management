# Supermarket Management System

This is a simple C++ console application to simulate a basic supermarket management system. The system allows administrators to manage products by adding, editing, and deleting them, while buyers can view and purchase products.

## Features

1. **Administrator Functions:**
    - Add new products.
    - Edit existing products.
    - Delete products.

2. **Buyer Functions:**
    - View the list of available products.
    - Purchase products and generate a receipt.

## Class Overview

### `shopping` Class

The `shopping` class encapsulates the entire functionality of the supermarket management system.

#### Private Members:
- `int pcode`: Product code.
- `float price`: Product price.
- `float dis`: Discount on the product.
- `string pname`: Product name.

#### Public Methods:

- **Virtual Function:**
    - `void displayDetails()`: Displays product details.

- **Friend Function:**
    - `friend void printDetails(const shopping &item)`: Friend function to print product details.

- **Menu Functions:**
    - `void menu()`: Displays the main menu for the application.
    - `void administrator()`: Displays the administrator menu.
    - `void buyer()`: Displays the buyer menu.

- **Product Management Functions:**
    - `void add()`: Adds a new product to the system.
    - `void edit()`: Edits an existing product.
    - `void rem()`: Removes a product from the system.
    - `void list()`: Lists all the products.
    - `void receipt()`: Generates a receipt for the purchased products.

## Function Descriptions

### `void displayDetails()`
This virtual function prints the details of a product, including the product code, name, price, and discount.

### `void printDetails(const shopping &item)`
This friend function prints the details of a given `shopping` object.

### `void menu()`
Displays the main menu where the user can choose between the administrator or buyer functionalities or exit the program.

### `void administrator()`
Displays the administrator menu with options to add, edit, delete products, or return to the main menu.

### `void buyer()`
Displays the buyer menu with options to buy products or go back to the main menu.

### `void add()`
Prompts the administrator to enter product details and saves the new product to a file called `database.txt`. It ensures no duplicate product codes are added.

### `void edit()`
Allows the administrator to modify an existing product's details based on the product code. Updates the product details in the file `database.txt`.

### `void rem()`
Allows the administrator to delete a product based on the product code. Removes the product from the file `database.txt`.

### `void list()`
Lists all the products by reading from the file `database.txt`.

### `void receipt()`
Generates a receipt for the buyer. It prompts the buyer to enter product codes and quantities, calculates the total amount with discounts, and displays the receipt.

## Usage

### Compilation
To compile the program, use a C++ compiler like `g++`:

```sh
g++ -o supermarket supermarket.cpp
```

### Execution
Run the compiled executable:

```sh
./supermarket
```

Follow the on-screen prompts to navigate through the menus and perform the desired operations.

## Conclusion

This project provides a basic framework for a supermarket management system, demonstrating the use of file handling, friend functions, virtual functions, and basic menu-driven console applications in C++. Further enhancements can include more robust error handling, data validation, and a more sophisticated user interface.
