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

Общая
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| backOfficeTop | header.inc.php | Yes | Вызывается с заголовком, над вкладками. |
| backOfficeHeader | header.inc.php | No | Вызывается между тегами HEAD. Идеальное место для добавления файлов JavaScript и CSS. |
| backOfficeFooter | footer.inc.php | Yes | Вызывается в footer страницы над строкой «Power By PrestaShop». |
| backOfficeHome | index.php | Yes | Вызывается в центре домашней страницы. |

Заказы и детали заказа
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| newOrder | Class: PaymentModule.php | No | Вызывается во время создания нового заказа сразу после его создания. |
| paymentConfirm | Class: Hook.php | No | Вызывается, когда статус заказа становится «Платеж принят». |
| updateOrderStatus | Class: OrderHistory.php | No | Вызывается при изменении статуса заказа, непосредственно перед его фактическим изменением. |
| postUpdateOrderStatus | Class: OrderHistory.php | No | Вызывается при изменении статуса заказа сразу после его фактического изменения. |
| cancelProduct | AdminOrders.php | No | Вызывается, когда элемент удаляется из заказа, сразу после удаления. |
| invoice | AdminOrders.php | Yes | Вызывается, когда отображаются подробности заказа, выше блока информации о клиенте. |
| adminOrder | AdminOrders.php | Yes | Вызывается, когда отображаются детали заказа, под блоком информации о клиенте. |
| orderSlip | AdminOrders.php | No | Вызывается во время создания кредитной карты сразу после ее создания. |

Товары
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| addproduct | AdminProducts.php | No | Вызывается, когда продукт создается или дублируется, сразу после указанного создания / дублирования. |
| updateproduct | AdminProducts.php | No | Вызывается, когда продукт обновляется с новой картинкой, сразу после указанного обновления. |
| deleteproduct | Class: Product.php | No | Вызывается при удалении продукта, прямо перед указанным удалением. |
| updateQuantity | Class: PaymentModule.php | No | Вызывается во время проверки заказа, состояние которого равно «отменен» или «ошибка платежа» для каждого из элементов заказа. |
| updateProductAttribute | Class: Product.php | No | Вызывается при обновлении склонения продукта сразу после указанного обновления. |
| watermark | AdminProducts.php | No | Вызывается, когда изображение добавляется в продукт, сразу после указанного добавления. |

Статистика
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| GraphEngine | Class: ModuleGraph.php | Yes | Вызывается, когда отображается график статистики. |
| GridEngine | Module: GridEngine.php | Yes | Вызывается, когда отображается сетка статистики. |
| AdminStatsModules | AdminStatsTab.php | Yes | Вызывается, когда отображается список модулей статистики. |

Клиенты
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| adminCustomers | AdminCustomers.php | Yes | Вызывается, когда отображаются данные клиента, сразу после списка групп клиентов, к которому принадлежит текущий клиент. |

Перевозчики
-------

| Hook name | File location | Visible | Description |
| --- | --- | --- | --- |
| updateCarrier | AdminCarriers.php | No | Вызывается во время обновления оператора, сразу после указанного обновления. |
