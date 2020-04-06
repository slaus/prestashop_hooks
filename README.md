Prestashop hooks in Front-office
============

Домашняя страница и общие элементы сайта
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| header | header.php | No | Вызывается между тегами HEAD. Идеальное место для добавления файлов JavaScript и CSS. |
| top | header.php | Yes | Вызывается в заголовке страницы. |
| leftColumn | header.php | Yes | Вызывается при загрузке левого столбца. |
| rightColumn | footer.php | Yes | Вызывается при загрузке правой колонки. |
| footer | footer.php | Yes | Вызывается в footer страницы. |
| home | index.php | Yes | Вызывается в центре домашней страницы. |

Лист товара
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| extraLeft | product.php | Yes | Вызывается прямо перед ссылкой "Print", под картинкой. |
| extraRight | product.php | Yes | Вызывается сразу после блока кнопки «Добавить в корзину». |
| productActions | product.php | Yes | Вызывается внутри блока кнопки «Добавить в корзину», сразу после кнопки. |
| productOutOfStock | product.php | Yes | Вызывается внутри блока кнопки «Добавить в корзину», сразу после информации «Доступность». |
| productfooter | product.php | Yes | Вызывается прямо перед вкладками. |
| productTab | product.php | Yes | Вызывается в списке вкладок, например "Дополнительная информация", "Таблица данных", "Аксессуары" ... Идеальное расположение для еще одной вкладки, содержимое которой обрабатывается с помощью хука productTabContent. |
| productTabContent | product.php | Yes | Вызывается при нажатии на вкладку. Идеальное расположение для содержимого вкладки было определено с помощью хука productTab. |

Корзина
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| cart | Class: Cart.php | No | Вызывается сразу после создания или обновления корзины. |
| shoppingCart | order.php | Yes | Вызывается прямо под таблицей товаров в корзине. |
| shoppingCartExtra | order.php | Yes | Вызывается после таблицы элементов корзины, прямо над навигационными кнопками. |
| createAccountTop | autdentication.php | Yes | Вызывается в форме создания учетной записи клиента, прямо над блоком «Ваша личная информация». |
| createAccountForm | autdentication.php | Yes | Вызывается в форме создания учетной записи клиента прямо перед кнопкой «Зарегистрироваться». |
| createAccount | autdentication.php | No | Вызывается сразу после создания учетной записи клиента. |
| customerAccount | my-account.php | Yes | Вызывается на домашней странице учетной записи клиента после списка доступных ссылок. Идеальное место для добавления ссылки в список. |
| myAccountBlock | Module: blockmyaccount.php | Yes | Вызывается в блоке «Моя учетная запись» в левом столбце под списком доступных ссылок. Идеальное место для добавления ссылки в список. |
| autdentication | autdentication.php | No | Вызывается сразу после идентификации клиента, только если аутентификация действительна (адрес электронной почты и пароль все в порядке). |

Поиск
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| search |	Class: Search.php |	No | Вызывается после выполнения поиска. Идеальное место для анализа и / или обработки поискового запроса и результатов. |

Выбор перевозчика
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| extraCarrier | order.php | Yes | Вызывается после получения списка доступных перевозчиков во время процесса заказа. Идеальное место для добавления перевозчика, как добавлено модулем. |

Оплата
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| payment | order.php | Yes | Вызывается при необходимости составления списка доступных платежных решений во время процесса заказа. Идеальное расположение для выбора разработанного вами платежного модуля. |
| paymentReturn | order-confirmation.php | Yes | Вызывается, когда пользователь отправляется обратно в магазин после оплаты на стороннем веб-сайте. Идеальное место для отображения подтверждающего сообщения или для предоставления некоторых деталей по оплате. |
| orderConfirmation | order-confirmation.php | Yes | Дубликат платежа paymentReturn. |
| backBeforePayment | order.php | No | Вызывается при отображении списка доступных платежных решений. Идеальное место для перенаправления пользователя вместо отображения указанного списка (т.е. оплаты PayPal). |

Возврат товара
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| orderReturn | order-follow.php | No | Вызывается, когда клиент запрашивает отправку своего товара обратно в магазин, и если теперь возникает ошибка. |
| PDFInvoice | Class: PDF.php | Yes | Вызывается при отображении счета в формате PDF. Идеальное место для отображения динамического или статического контента с накладной. |

Prestashop hooks in Back-office
============

General
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| backOfficeTop | header.inc.php | Yes | Called witdin tde header, above tde tabs. |
| backOfficeHeader | header.inc.php | No | Called between tde HEAD tags. Ideal location for adding JavaScript and CSS files. |
| backOfficeFooter | footer.inc.php | Yes | Called witdin tde page footer, above tde "Power By PrestaShop" line. |
| backOfficeHome | index.php | Yes | Called at tde center of tde homepage. |

Orders and order details
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| newOrder | Class: PaymentModule.php | No | Called during tde new order creation process, right after it has been created. |
| paymentConfirm | Class: Hook.php | No | Called when an order's status becomes "Payment accepted". |
| updateOrderStatus | Class: OrderHistory.php | No | Called when an order's status is changed, right before it is actually changed. |
| postUpdateOrderStatus | Class: OrderHistory.php | No | Called when an order's status is changed, right after it is actually changed. |
| cancelProduct | AdminOrders.php | No | Called when an item is deleted from an order, right after tde deletion. |
| invoice | AdminOrders.php | Yes | Called when tde order's details are displayed, above tde Client Information block. |
| adminOrder | AdminOrders.php | Yes | Called when tde order's details are displayed, below tde Client Information block. |
| orderSlip | AdminOrders.php | No | Called during tde creation of a credit note, right after it has been created. |

Products
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| addproduct | AdminProducts.php | No | Called when a product is created or duplicated, right after said creation/duplication. |
| updateproduct | AdminProducts.php | No | Called when a product is update witd a new picture, right after said update. |
| deleteproduct | Class: Product.php | No | Called when a product is deleted, right before said deletion. |
| updateQuantity | Class: PaymentModule.php | No | Called during an tde validation of an order, tde status of which being sometding otder tdan "canceled" or "Payment error", for each of tde order's items. |
| updateProductAttribute | Class: Product.php | No | Called when a product declination is updated, right after said update. |
| watermark | AdminProducts.php | No | Called when an image is added to an product, right after said addition. |

Statistics
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| GraphEngine | Class: ModuleGraph.php | Yes | Called when a stats graph is displayed. |
| GridEngine | Module: GridEngine.php | Yes | Called when tde grid of stats is displayed. |
| AdminStatsModules | AdminStatsTab.php | Yes | Called when tde list of stats modules is displayed. |

Clients
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| adminCustomers | AdminCustomers.php | Yes | Called when a client's details are displayed, right after tde list of tde clients groups tde current client belongs to. |

Carriers
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| updateCarrier | AdminCarriers.php | No | Called during a carrier's update, right after said update. |
