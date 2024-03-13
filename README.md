# New-York-Jobs-CEO-Council-Software-Engineering-Job-Simulation

## Task 1 Overview
Spinvoice is a billing system designed to automatically generate invoices. However, a recent bug has been identified in the codebase related to the way discounts are applied to the final price of the invoice.

## Bug Description
The bug occurs in the `calculate_total` method of the `Invoice` class. When calculating the total amount of the invoice, the current implementation applies the discount incorrectly, resulting in an incorrect final price.

## Bug Fix
To fix the bug, the discount should be applied to the total price of each individual item before summing up all item totals. The corrected equation ensures that the discount is applied accurately to each item's total price.

```python
item_total_price = price + (price * tax)  # Calculate the total price of the item including tax
total_discount = item_total_price * (discount / 100)  # Calculate the discount amount for the item
total += item_total_price - total_discount  # Subtract the discount from the total item price and add to the invoice total
```

## Usage
To use the fixed version of the `Invoice` class:
1. Instantiate an `Invoice` object with sender and recipient details.
2. Add items to the invoice using the `add_item` method, providing the item name, price, and tax rate.
3. Call the `calculate_total` method, passing the discount percentage as an argument.
4. The method will return the corrected total amount to pay, considering the applied discount.

## Conclusion
With the bug fixed, the Spinvoice billing system will accurately calculate the total amount to be paid on invoices, ensuring reliable and correct billing for clients.

## Task 2 Overview
As part of enhancing the functionality of the Spinvoice billing system, I've implemented a new feature to allow attaching comments to invoices.

## Changes Made
To support comments in invoices, I added the following methods to the `Invoice` class:
- `add_comment(comment)`: This method allows adding a new comment to the invoice.
- `get_comments()`: This method returns a string representation of all comments associated with the invoice.

## Usage
Adding comments to invoices and retrieving them is straightforward:
1. Create an `Invoice` object with sender and recipient details.
2. Add items to the invoice using the `add_item` method, providing the item name, price, and tax rate.
3. Call the `add_comment` method to add any relevant comments to the invoice.
4. To retrieve all comments associated with the invoice, use the `get_comments` method.

## Conclusion
With the new comments feature implemented, users can now easily attach relevant notes to invoices, facilitating better communication and understanding of charges. This enhancement improves the overall functionality and usability of the Spinvoice billing system.

