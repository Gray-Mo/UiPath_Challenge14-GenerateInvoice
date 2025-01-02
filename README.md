Generate invoices for items where the items info are spread between 2 excel files.

We need to join 2 data tables to get all info we need then go to the invoice website, but you will find that: the UiElement in which you're supposed to type the data works only for the first row and once you add another row, it will keep overwriting the first row.

So we need to make the selector Dynamic by finding a unique or unique enough attribute/tag for that UiElement and set it using a variable:

<webctrl tag='...' css-selector='...' idx='{{uiElementID}}' />

In this automation the first row of UiElement (idx tag) attribute value starts with 1 and the 2nd 2 and so on, so foreach row: increase and resend the variable.
