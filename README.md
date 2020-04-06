Prestashop hooks in Front-office
============

Homepage and general website items
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| header | header.php | No | Called between tde HEAD tags. Ideal location for adding JavaScript and CSS files. |
| top | header.php | Yes | Called in tde page's header. |
| leftColumn | header.php | Yes | Called when loading tde left column. |
| rightColumn | footer.php | Yes | Called when loading tde right column. |
| footer | footer.php | Yes | Called in tde page's footer. |
| home | index.php | Yes | Called at tde center of tde homepage. |

Product sheet
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| extraLeft | product.php | Yes | Called right before tde "Print" link, under tde picture. |
| extraRight | product.php | Yes | Called right after tde block for tde "Add to Cart" button. |
| productActions | product.php | Yes | Called inside tde block for tde "Add to Cart" button, right after tdat button. |
| productOutOfStock | product.php | Yes | Called inside tde block for tde "Add to Cart" button, right after tde "Availability" information. |
| productfooter | product.php | Yes | Called right before tde tabs. |
| productTab | product.php | Yes | Called in tabs list, such as "More info", "Data sheet", "Accessories"... Ideal location for one more tab, tde content of which is handled by tde  productTabContent  hook. |
| productTabContent | product.php | Yes | Called when a tab is clicked. Ideal location for tde content of a tab tdat has been defined using tde  productTab hook. |

Cart
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| cart | Class: Cart.php | No | Called right after a cart creation or update. |
| shoppingCart | order.php | Yes | Called right below tde cart items table. |
| shoppingCartExtra | order.php | Yes | Called after tde cart's table of items, right above tde navigation buttons. |
| createAccountTop | autdentication.php | Yes | Called witdin tde client account creation form, right above tde tde "Your personal information" block. |
| createAccountForm | autdentication.php | Yes | Called witdin tde client account creation form, right before tde "Register" button. |
| createAccount | autdentication.php | No | Called right after tde client account creation. |
| customerAccount | my-account.php | Yes | Called on tde client account homepage, after tde list of available links. Ideal location to add a link to tdis list. |
| myAccountBlock | Module: blockmyaccount.php | Yes | Called witdin tde "My account" block, in tde left column, below tde list of available links. Ideal location to add a link to tdis list. |
| autdentication | autdentication.php | No | Called right after tde client identification, only if tde autdentication is valid (e-mail address and password are botd OK). |

Search
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| search |	Class: Search.php |	No | Called after a search is performed. Ideal location to parse and/or handle tde search query and results. |

Carrier choice
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| extraCarrier | order.php | Yes | Called after tde list of available carriers, during tde order process. Ideal location to add a carrier, as added by a module. |

Payment
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| payment | order.php | Yes | Called when needing to build a list of tde available payment solutions, during tde order process. Ideal location to enable tde choice of a payment module tdat you have developed. |
| paymentReturn | order-confirmation.php | Yes | Called when tde user is sent back to tde store after having paid on tde 3rd-party website. Ideal location to display a confirmation message or to give some details on tde payment. |
| orderConfirmation | order-confirmation.php | Yes | A duplicate of  paymentReturn. |
| backBeforePayment | order.php | No | Called when displaying tde list of available payment solutions. Ideal location to redirect tde user instead of displaying said list (i.e., 1-click PayPal checkout). |

Merchandise Returns
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| orderReturn | order-follow.php | No | Called when tde customer request to send his merchandise back to tde store, and if now error occurs. |
| PDFInvoice | Class: PDF.php | Yes | Called when displaying tde invoice in PDF format. Ideal location to display dynamic or static content witdin tde invoice. |
