# sales-taxes-rep
Problem

Basic sales tax is applicable at a rate of 10% on all goods, except books, food, and medical products that are exempt. Import duty is an additional sales tax applicable on all imported goods at a rate of 5%, with no exemptions.

When I purchase items I receive a receipt which lists the name of all the items and their price (including tax), finishing with the total cost of the items, and the total amounts of sales taxes paid. The rounding rules for sales tax are that for a tax rate of n%, a shelf price of p contains (np/100 rounded up to the nearest 0.05) amount of sales tax.

Write an application that prints out the receipt details for these shopping baskets...

INPUT:

Input 1:
1 book at 12.49
1 music CD at 14.99
1 chocolate bar at 0.85

Input 2:
1 imported box of chocolates at 10.00
1 imported bottle of perfume at 47.50

Input 3:
1 imported bottle of perfume at 27.99
1 bottle of perfume at 18.99
1 packet of headache pills at 9.75
1 box of imported chocolates at 11.25

OUTPUT

Output 1:
1 book : 12.49
1 music CD: 16.49
1 chocolate bar: 0.85
Sales Taxes: 1.50
Total: 29.83

Output 2:
1 imported box of chocolates: 10.50
1 imported bottle of perfume: 54.65
Sales Taxes: 7.65
Total: 65.15

Output 3:
1 imported bottle of perfume: 32.19
1 bottle of perfume: 20.89
1 packet of headache pills: 9.75
1 imported box of chocolates: 11.85
Sales Taxes: 6.70
Total: 74.68

Solution contains:

Item class;
Basket class;
BasketFiller class;
IReceiptPrinter interface;
ReceiptPrintes class;
App class;
AppTest class.



The “Item” object represents the goods with his properties. This class expose three utility methods:
•	calculateItemSalesTax(); that verifies if an item is exempt or not and if an item is imported or not, and returns the item sales taxes;

•	calculateFees(); that calculates the item fee amount;

•	calculateItemPriceWithTax(): that calculates the item price with taxes.


The “Basket” object represents a list of items. This class expose two methods to add/remove items from a basket:
•	addItem(Item item);

•	removeItem(Item item).

The “BasketFiller” class exposes fillBaskets() method to fill n baskets with items (In this case three baskets are filled ) and returns a basket’s list.

The “ReceiptPrinter” class implements IReceiptPrinter.printReceipt(List<Basket> basketList) method that prints receipts for the baskets given in input.

The App class represents the application entry point, which initializes data by calling BasketFiller.fillBaskets() method, than prints receipts by calling ReceiptPrinter.printReceipt() method.

The  AppTest class represents a junit test.





