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
