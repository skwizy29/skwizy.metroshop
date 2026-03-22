Skwizy
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>SkwizyShop | Metro Royale предметы PUBG Mobile</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Poppins', 'Inter', system-ui, -apple-system, BlinkMacSystemFont, 'Roboto', sans-serif;
        }

        body {
            background: radial-gradient(circle at 10% 20%, #0a0f1e, #03060c);
            color: #eef2ff;
            padding: 1rem;
            min-height: 100vh;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
        }

        .header {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            gap: 20px;
            margin-bottom: 30px;
            background: rgba(10, 20, 30, 0.65);
            backdrop-filter: blur(12px);
            border-radius: 3rem;
            padding: 0.8rem 2rem;
            border: 1px solid rgba(255, 215, 0, 0.25);
            box-shadow: 0 10px 25px -5px rgba(0,0,0,0.5);
        }

        .logo h1 {
            font-size: 2rem;
            background: linear-gradient(135deg, #F5AF19, #f0c45a);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            letter-spacing: 1px;
        }
        .logo p {
            font-size: 0.75rem;
            color: #b9c7d9;
        }

        .cart-icon {
            background: #11161f;
            padding: 10px 20px;
            border-radius: 40px;
            display: flex;
            align-items: center;
            gap: 12px;
            cursor: pointer;
            transition: 0.2s;
            border: 1px solid #2a3a44;
            box-shadow: 0 4px 12px rgba(0,0,0,0.4);
        }
        .cart-icon:hover {
            background: #1e2a36;
            transform: scale(1.02);
            border-color: #f5b81b;
        }
        .cart-icon span:first-child {
            font-size: 1.6rem;
        }
        .cart-count {
            background: #f5b81b;
            color: #0a0c15;
            font-weight: bold;
            border-radius: 30px;
            padding: 2px 10px;
            font-size: 1rem;
        }
        .cart-price {
            font-weight: 600;
            background: #00000055;
            padding: 4px 12px;
            border-radius: 32px;
        }

        .support-bar {
            display: flex;
            justify-content: flex-end;
            margin-bottom: 15px;
            gap: 15px;
            flex-wrap: wrap;
        }
        .support-card {
            background: #0f1722cc;
            backdrop-filter: blur(8px);
            padding: 8px 20px;
            border-radius: 60px;
            font-size: 0.85rem;
            border: 1px solid #f5b81b55;
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }
        .support-card span:first-child {
            font-size: 1.2rem;
        }
        .support-card .phone-num {
            font-weight: bold;
            color: #f5c542;
            letter-spacing: 1px;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 28px;
            margin: 30px 0;
        }

        .product-card {
            background: linear-gradient(145deg, #11171f, #0b1017);
            border-radius: 2rem;
            overflow: hidden;
            transition: all 0.25s ease;
            border: 1px solid #2a3743;
            backdrop-filter: blur(4px);
            box-shadow: 0 20px 30px -15px black;
        }
        .product-card:hover {
            transform: translateY(-6px);
            border-color: #f5b81b80;
            box-shadow: 0 25px 35px -12px #000000cc;
        }

        .product-img {
            height: 170px;
            background: #1f2a33;

Сиська,
display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4.5rem;
            border-bottom: 1px solid #2f3e4a;
        }

        .product-info {
            padding: 1.2rem;
        }
        .product-title {
            font-size: 1.4rem;
            font-weight: 700;
            margin-bottom: 6px;
            display: flex;
            justify-content: space-between;
        }
        .product-category {
            font-size: 0.7rem;
            text-transform: uppercase;
            background: #1e2a32;
            display: inline-block;
            padding: 2px 10px;
            border-radius: 20px;
            color: #cddcec;
            margin-bottom: 10px;
        }
        .product-desc {
            font-size: 0.85rem;
            color: #b0c4de;
            margin: 10px 0;
        }
        .product-price {
            font-size: 1.7rem;
            font-weight: bold;
            color: #f5c542;
            margin: 12px 0;
        }
        .btn-add {
            background: #f5b81b;
            border: none;
            width: 100%;
            padding: 12px;
            font-weight: bold;
            font-size: 1rem;
            border-radius: 60px;
            color: #0b0f17;
            cursor: pointer;
            transition: 0.2s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }
        .btn-add:hover {
            background: #ffce4a;
            transform: scale(0.98);
            box-shadow: 0 4px 12px rgba(245,184,27,0.4);
        }

        /* Модалка корзины */
        .cart-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.85);
            backdrop-filter: blur(8px);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }
        .cart-modal.active {
            display: flex;
        }
        .cart-panel {
            background: #0e141f;
            width: 90%;
            max-width: 700px;
            max-height: 85vh;
            border-radius: 2rem;
            padding: 1.5rem;
            border: 1px solid #ffd966;
            overflow-y: auto;
            box-shadow: 0 30px 40px black;
        }

        /* Модалка оплаты */
        .payment-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.95);
            backdrop-filter: blur(12px);
            z-index: 1100;
            justify-content: center;
            align-items: center;
        }
        .payment-modal.active {
            display: flex;
        }
        .payment-panel {
            background: linear-gradient(145deg, #111a24, #0a0f18);
            width: 90%;
            max-width: 500px;
            border-radius: 2rem;
            padding: 2rem;
            border: 1px solid #f5c542;
            box-shadow: 0 0 40px rgba(245, 184, 27, 0.3);
            text-align: center;
        }
        .payment-panel h2 {
            color: #f5c542;
            margin-bottom: 20px;
            font-size: 1.8rem;
        }
        .payment-amount {
            font-size: 2.5rem;
            font-weight: bold;
            background: #00000055;
            padding: 15px;
            border-radius: 1.5rem;
            margin: 20px 0;
            color: #ffdf8c;
        }
        .payment-card-details {
            background: #071017;
            border-radius: 1.2rem;
            padding: 20px;
            margin: 20px 0;
            border: 1px solid #f5b81b55;
        }
        .payment-card-number {
            font-size: 1.6rem;
            font-family: monospace;
            font-weight: bold;
            letter-spacing: 2px;
            background: #00000066;
            padding: 12px;
            border-radius: 1rem;

Сиська, [23.03.2026 01:34]
margin: 10px 0;
            color: #ffde9c;
            word-break: break-all;
        }
        .payment-support {
            background: #1a2530;
            border-radius: 1rem;
            padding: 12px;
            margin: 15px 0;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }
        .copy-big-btn {
            background: #f5b81b;
            border: none;
            padding: 12px 24px;
            border-radius: 60px;
            font-weight: bold;
            font-size: 1rem;
            cursor: pointer;
            margin-top: 10px;
            transition: 0.2s;
        }
        .copy-big-btn:hover {
            background: #ffce4a;
            transform: scale(1.02);
        }
        .close-payment-btn {
            background: #2c3e44;
            border: none;
            padding: 10px 20px;
            border-radius: 40px;
            color: white;
            cursor: pointer;
            margin-top: 15px;
        }
        .paid-btn {
            background: #27ae60;
            border: none;
            padding: 12px 28px;
            border-radius: 60px;
            font-weight: bold;
            color: white;
            cursor: pointer;
            margin-top: 15px;
            width: 100%;
            font-size: 1.1rem;
        }
        .cart-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 2px solid #2d3e4e;
            padding-bottom: 12px;
            margin-bottom: 20px;
        }
        .close-cart {
            background: none;
            border: none;
            font-size: 2rem;
            cursor: pointer;
            color: #f0c45a;
        }
        .cart-items-list {
            list-style: none;
            margin: 15px 0;
            max-height: 45vh;
            overflow-y: auto;
        }
        .cart-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: #0a111a;
            margin: 8px 0;
            padding: 12px;
            border-radius: 1.2rem;
            border-left: 4px solid #f5b81b;
        }
        .item-info h4 {
            font-size: 1rem;
        }
        .item-price {
            font-weight: bold;
            color: #f5c542;
        }
        .item-actions button {
            background: #2c3e44;
            border: none;
            color: white;
            font-weight: bold;
            width: 28px;
            border-radius: 30px;
            margin: 0 3px;
            cursor: pointer;
        }
        .cart-total {
            text-align: right;
            font-size: 1.5rem;
            border-top: 1px solid #2e4a5a;
            padding-top: 15px;
            margin-top: 10px;
        }
        .payment-section {
            background: #071017;
            border-radius: 1.5rem;
            padding: 1rem;
            margin-top: 20px;
        }
        .pay-methods {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
            margin: 12px 0;
        }
        .method-btn {
            background: #1b2a33;
            border: none;
            padding: 8px 16px;
            border-radius: 40px;
            color: white;
            cursor: pointer;
            transition: 0.1s;
        }
        .method-btn.active {
            background: #f5b81b;
            color: #0a0c15;
            font-weight: bold;
        }
        .order-btn {
            background: #27ae60;
            width: 100%;
            padding: 14px;
            font-weight: bold;
            border: none;
            border-radius: 60px;
            font-size: 1.1rem;
            color: white;
            cursor: pointer;
            margin-top: 15px;
        }
        .toast-msg {
            position: fixed;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            background: #1f2c38e6;

Сиська, [23.03.2026 01:34]
backdrop-filter: blur(12px);
            padding: 12px 28px;
            border-radius: 60px;
            color: #ffdf8c;
            font-weight: bold;
            z-index: 1200;
            border-left: 4px solid gold;
            pointer-events: none;
        }
        .empty-cart {
            text-align: center;
            padding: 30px;
            color: #9aaec2;
        }
        footer {
            text-align: center;
            margin-top: 50px;
            padding: 20px;
            font-size: 0.8rem;
            opacity: 0.7;
        }
        button {
            cursor: pointer;
        }
        @media (max-width: 650px) {
            .header {
                flex-direction: column;
                text-align: center;
            }
            .support-bar {
                justify-content: center;
            }
            .payment-card-number {
                font-size: 1.2rem;
            }
        }
    </style>
</head>
<body>
<div class="container">
    <div class="support-bar">
        <div class="support-card">
            <span>📞</span> Поддержка: <span class="phone-num" id="supportPhone">+79997818232</span>
            <button class="copy-btn" data-copy="+79997818232" style="background:#2c3e44; margin-left:5px;">📋</button>
        </div>
        <div class="support-card">
            <span>💳</span> Карта для оплаты: <span class="card-number" id="bankCard">2200701230844117</span>
            <button class="copy-btn" data-copy="2200701230844117" style="background:#2c3e44;">📋</button>
        </div>
    </div>

    <div class="header">
        <div class="logo">
            <h1>⚡ SKWIZYSHOP</h1>
            <p>Metro Royale • Сопровождение • Оружейные контракты • Реликвии</p>
        </div>
        <div class="cart-icon" id="openCartBtn">
            <span>🛒</span>
            <span class="cart-count" id="cartCount">0</span>
            <span class="cart-price" id="cartTotalPreview">0₽</span>
        </div>
    </div>

    <div class="products-grid" id="productsGrid"></div>
    <footer>© SkwizyShop — официальный трансфер Metro Royale. Мгновенная доставка после оплаты.</footer>
</div>

<!-- Модалка корзины -->
<div id="cartModal" class="cart-modal">
    <div class="cart-panel">
        <div class="cart-header">
            <h2>🧾 Ваша корзина</h2>
            <button class="close-cart" id="closeCartBtn">&times;</button>
        </div>
        <div id="cartItemsContainer" class="cart-items-list"></div>
        <div class="cart-total" id="cartTotalAmount">Итого: 0₽</div>
        <div class="payment-section">
            <h3>💳 Способ оплаты</h3>
            <div class="pay-methods" id="payMethodsContainer">
                <button data-method="card" class="method-btn active">💳 Банковская карта</button>
                <button data-method="qiwi" class="method-btn">🟣 QIWI / ЮMoney</button>
                <button data-method="crypto" class="method-btn">₿ USDT / Crypto</button>
            </div>
            <div id="paymentInfoMsg" style="font-size:0.8rem; margin: 8px 0; color:#c0d4f0;">✅ Быстрая защищенная оплата</div>
            <button class="order-btn" id="checkoutBtn">✅ Оформить заказ</button>
        </div>
    </div>
</div>

<!-- Модалка ОПЛАТЫ (перекидывает сюда после оформления) -->
<div id="paymentModal" class="payment-modal">
    <div class="payment-panel">
        <h2>💸 ОПЛАТА ЗАКАЗА</h2>
        <p>Для завершения покупки переведите сумму на карту</p>
        <div class="payment-amount" id="paymentAmountDisplay">0 ₽</div>
        <div class="payment-card-details">
            <span style="font-size:0.9rem;">💳 Карта получателя:</span>
            <div class="payment-card-number" id="paymentCardNumber">2200701230844117</div>
            <button class="copy-big-btn" id="copyCardFromPayment">📋 Скопировать номер карты</button>
        </div>
        <div class="payment-support">
            <span>📞 Поддержка: </span>
            <strong id="paymentSupportPhone">+79997818232</strong>

Сиська, [23.03.2026 01:34]
<button class="copy-btn" data-copy="+79997818232" style="background:#1f2a33;">Копировать</button>
        </div>
        <p style="font-size:0.8rem; margin: 10px 0;">После оплаты нажмите "Я оплатил(а)", чтобы подтвердить заказ</p>
        <button class="paid-btn" id="confirmPaymentBtn">✅ Я оплатил(а)</button>
        <button class="close-payment-btn" id="closePaymentBtn">✖️ Закрыть</button>
    </div>
</div>

<div id="toast" class="toast-msg" style="display: none;"></div>

<script>
    const PRODUCTS = [
        { id: 1, name: "🛡️ Сопровод 'Стальной Страж'", category: "Сопровождение", desc: "Опытный телохранитель, помогает в рейдах метро, прикрывает от рейдеров. 1 рейд", price: 199, icon: "🛡️" },
        { id: 2, name: "🔍 Сопровод 'Теневой Разведчик'", category: "Сопровождение", desc: "Сканирует локацию, показывает тайники и врагов. Эффективная разведка на 2 рейда", price: 299, icon: "🔍" },
        { id: 3, name: "⚡ Сопровод 'Быстрый Курьер'", category: "Сопровождение", desc: "Ускоряет сбор лута + переносит ценные вещи. Экономия времени в метро", price: 249, icon: "⚡" },
        { id: 4, name: "MK14 'Метро Легенда'", category: "Оружие", desc: "Эксклюзивная винтовка с улучшенной бронепробиваемостью, х2 модуль", price: 1290, icon: "🔫" },
        { id: 5, name: "Бронекостюм 'Стальной Шторм'", category: "Снаряжение", desc: "Lv.6 бронежилет + шлем, защита от эксп. урона", price: 890, icon: "🛡️" },
        { id: 6, name: "Рюкзак 'Сектор 7'", category: "Снаряжение", desc: "Увеличенная вместимость + защита от мародеров", price: 490, icon: "🎒" },
        { id: 7, name: "Аптечка 'Феникс' x5", category: "Расходники", desc: "Мгновенное восстановление HP + адреналин", price: 350, icon: "💊" },
        { id: 8, name: "M762 'Золотой Тигр'", category: "Оружие", desc: "Скин легендарный + повышенный урон по боссам", price: 1590, icon: "🐅" },
        { id: 9, name: "Подавитель нового поколения", category: "Модули", desc: "Бесшумный выстрел + на 15% больше урона", price: 720, icon: "🔇" },
        { id: 10, name: "Баллистический щит", category: "Снаряжение", desc: "Экзощит для штурма метро, повышенная мобильность", price: 1100, icon: "🛡️" },
        { id: 11, name: "Редкий ящик 'Метро Реликвия'", category: "Контейнер", desc: "Гарантированный легендарный лут + скины оружия", price: 2490, icon: "🎁" }
    ];

    let cart = [];
    let currentPaymentMethod = "card";
    let pendingOrderTotal = 0;

    function loadCartFromStorage() {
        const stored = localStorage.getItem("skwizy_cart");
        if(stored) {
            try {
                cart = JSON.parse(stored);
                if(!Array.isArray(cart)) cart = [];
            } catch(e) { cart = []; }
        } else { cart = []; }
        cart = cart.filter(item => item && typeof item.id === 'number' && item.quantity > 0);
        renderCartBadge();
    }

    function saveCartToStorage() {
        localStorage.setItem("skwizy_cart", JSON.stringify(cart));
        renderCartBadge();
    }

    function renderCartBadge() {
        const totalCount = cart.reduce((sum, it) => sum + it.quantity, 0);
        const totalPrice = cart.reduce((sum, it) => sum + (it.price * it.quantity), 0);
        document.getElementById('cartCount').innerText = totalCount;
        document.getElementById('cartTotalPreview').innerHTML = totalPrice + "₽";
    }

    function getTotalPrice() {
        return cart.reduce((sum, it) => sum + (it.price * it.quantity), 0);
    }

    function addToCart(product) {
        const existing = cart.find(item => item.id === product.id);
        if(existing) existing.quantity += 1;
        else cart.push({ id: product.id, name: product.name, price: product.price, quantity: 1, icon: product.icon });
        saveCartToStorage();
        showToast(`✅ ${product.name} добавлен в корзину!`, 1500);
        if(document.getElementById('cartModal').classList.contains('active')) renderCartModalContent();
    }

    function updateQuantity(itemId, delta) {
        const idx = cart.findIndex(i => i.id === itemId);
        if(idx === -1) return;

Сиська, [23.03.2026 01:34]
const newQty = cart[idx].quantity + delta;
        if(newQty <= 0) cart.splice(idx,1);
        else cart[idx].quantity = newQty;
        saveCartToStorage();
        renderCartModalContent();
        if(cart.length === 0 && document.getElementById('cartModal').classList.contains('active')) renderCartModalContent();
    }

    function renderCartModalContent() {
        const container = document.getElementById('cartItemsContainer');
        if(!container) return;
        if(cart.length === 0) {
            container.innerHTML = <div class="empty-cart">🛒 Корзина пуста. Добавьте сопровождение, оружие или снаряжение!</div>;
            document.getElementById('cartTotalAmount').innerText = Итого: 0₽;
            return;
        }
        let itemsHtml = <ul style="list-style:none;">;
        cart.forEach(item => {
            const totalItemPrice = item.price * item.quantity;
            itemsHtml += `<li class="cart-item">
                <div class="item-info"><h4>${item.name}</h4><small>${item.price}₽ × ${item.quantity}</small></div>
                <div class="item-price">${totalItemPrice}₽</div>
                <div class="item-actions">
                    <button class="qty-minus" data-id="${item.id}">−</button>
                    <span style="margin:0 6px;">${item.quantity}</span>
                    <button class="qty-plus" data-id="${item.id}">+</button>
                    <button class="qty-remove" data-id="${item.id}" style="background:#aa2e2e;">🗑</button>
                </div>
            </li>`;
        });
        itemsHtml += </ul>;
        container.innerHTML = itemsHtml;
        document.getElementById('cartTotalAmount').innerHTML = Итого: ${getTotalPrice()}₽;

        document.querySelectorAll('.qty-plus').forEach(btn => btn.addEventListener('click', () => updateQuantity(parseInt(btn.dataset.id), 1)));
        document.querySelectorAll('.qty-minus').forEach(btn => btn.addEventListener('click', () => updateQuantity(parseInt(btn.dataset.id), -1)));
        document.querySelectorAll('.qty-remove').forEach(btn => btn.addEventListener('click', () => {
            const id = parseInt(btn.dataset.id);
            const idx = cart.findIndex(i => i.id === id);
            if(idx !== -1) cart.splice(idx,1);
            saveCartToStorage();
            renderCartModalContent();
            if(cart.length===0) renderCartBadge();
        }));
    }

    function initPaymentSelector() {
        const methods = document.querySelectorAll('.method-btn');
        methods.forEach(btn => {
            btn.addEventListener('click', () => {
                methods.forEach(m => m.classList.remove('active'));
                btn.classList.add('active');
                currentPaymentMethod = btn.dataset.method;
                const msgDiv = document.getElementById('paymentInfoMsg');
                if(currentPaymentMethod === 'card') msgDiv.innerHTML = '💳 Оплата картами Visa/Mastercard/Мир. Реквизиты: 2200701230844117';
                else if(currentPaymentMethod === 'qiwi') msgDiv.innerHTML = '🟣 Оплата через QIWI, ЮMoney на карту 2200701230844117';
                else msgDiv.innerHTML = '₿ Криптовалюта USDT (TRC20/BEP20). После оплаты подтверждение.';
            });
        });
    }

    function showToast(message, duration = 2500) {
        const toast = document.getElementById('toast');
        toast.innerText = message;
        toast.style.display = 'block';
        setTimeout(() => { toast.style.display = 'none'; }, duration);
    }

    // Открыть модалку оплаты с суммой заказа
    function openPaymentModal(totalAmount) {
        pendingOrderTotal = totalAmount;
        document.getElementById('paymentAmountDisplay').innerHTML = ${totalAmount} ₽;
        document.getElementById('paymentCardNumber').innerText = '2200701230844117';
        document.getElementById('paymentSupportPhone').innerText = '+79997818232';
        document.getElementById('paymentModal').classList.add('active');
    }

    // Закрыть модалку оплаты
    function closePaymentModal() {
        document.getElementById('paymentModal').

Сиська, [23.03.2026 01:34]
classList.remove('active');
    }

    // Подтверждение оплаты (очищаем корзину, показываем успех)
    function confirmPaymentAndClearCart() {
        if(pendingOrderTotal <= 0) {
            showToast("Нет активного заказа для подтверждения", 1500);
            closePaymentModal();
            return;
        }
        // Очистка корзины
        cart = [];
        saveCartToStorage();
        renderCartBadge();
        renderCartModalContent();
        // Закрыть все модалки
        closePaymentModal();
        const cartModal = document.getElementById('cartModal');
        if(cartModal.classList.contains('active')) cartModal.classList.remove('active');
        
        showToast(`✅ Спасибо за оплату! Сумма ${pendingOrderTotal}₽ получена. Предметы доставлены в игру в течение 2 минут.`, 5000);
        pendingOrderTotal = 0;
    }

    // Оформление заказа -> вместо старого toasta открываем модалку оплаты
    function processOrder() {
        if(cart.length === 0) {
            showToast("⚠️ Корзина пуста! Добавьте предметы.", 2000);
            return false;
        }
        const total = getTotalPrice();
        let methodName = "";
        if(currentPaymentMethod === "card") methodName = "Банковская карта";
        else if(currentPaymentMethod === "qiwi") methodName = "QIWI / ЮMoney";
        else methodName = "USDT / Криптовалюта";
        
        // Закрываем корзину и открываем модалку оплаты
        const cartModal = document.getElementById('cartModal');
        if(cartModal.classList.contains('active')) cartModal.classList.remove('active');
        
        openPaymentModal(total);
        showToast(`💸 Заказ на ${total}₽. Оплатите на карту в открывшемся окне. Способ: ${methodName}`, 4000);
        return true;
    }

    function renderProducts() {
        const grid = document.getElementById('productsGrid');
        if(!grid) return;
        grid.innerHTML = '';
        PRODUCTS.forEach(prod => {
            const card = document.createElement('div');
            card.className = 'product-card';
            card.innerHTML = `
                <div class="product-img">${prod.icon}</div>
                <div class="product-info">
                    <div class="product-title"><span>${prod.name}</span></div>
                    <div class="product-category">${prod.category}</div>
                    <div class="product-desc">${prod.desc}</div>
                    <div class="product-price">${prod.price} ₽</div>
                    <button class="btn-add" data-id="${prod.id}">➕ В корзину</button>
                </div>
            `;
            grid.appendChild(card);
            const btn = card.querySelector('.btn-add');
            btn.addEventListener('click', (e) => { e.stopPropagation(); addToCart(prod); });
        });
    }

    function bindModalControls() {
        const modal = document.getElementById('cartModal');
        const openBtn = document.getElementById('openCartBtn');
        const closeBtn = document.getElementById('closeCartBtn');
        openBtn.addEventListener('click', () => { renderCartModalContent(); modal.classList.add('active'); });
        closeBtn.addEventListener('click', () => modal.classList.remove('active'));
        modal.addEventListener('click', (e) => { if(e.target === modal) modal.classList.remove('active'); });
        document.getElementById('checkoutBtn').addEventListener('click', () => processOrder());
        
        // управление модалкой оплаты
        const paymentModal = document.getElementById('paymentModal');
        document.getElementById('closePaymentBtn').addEventListener('click', () => closePaymentModal());
        document.getElementById('confirmPaymentBtn').addEventListener('click', () => confirmPaymentAndClearCart());
        paymentModal.addEventListener('click', (e) => { if(e.target === paymentModal) closePaymentModal(); });
        
        // кнопка копирования внутри оплаты
        document.getElementById('copyCardFromPayment').addEventListener('click', () => {
            navigator.clipboard.writeText('2200701230844117').

Сиська, [23.03.2026 01:34]
then(() => showToast('💳 Номер карты скопирован!', 1200));
        });
    }

    function initCopyButtons() {
        const copyBtns = document.querySelectorAll('.copy-btn');
        copyBtns.forEach(btn => {
            btn.addEventListener('click', (e) => {
                e.stopPropagation();
                const text = btn.getAttribute('data-copy');
                if(text) navigator.clipboard.writeText(text).then(() => showToast(`📋 Скопировано: ${text}`, 1000));
            });
        });
    }

    function init() {
        loadCartFromStorage();
        renderProducts();
        bindModalControls();
        initPaymentSelector();
        initCopyButtons();
        console.log("SkwizyShop — готов! После оформления заказа открывается окно оплаты.");
    }
    init();
</script>
</body>
</html>
          
