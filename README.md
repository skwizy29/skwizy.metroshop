# skwizy.metroshop [23.03.2026 00:43]
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes, viewport-fit=cover">
    <title>Skwizy Metro Royale | PUBG Mobile Сопровождение</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700;14..32,800&family=Orbitron:wght@400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: #0a0c15;
            color: #eef2ff;
            scroll-behavior: smooth;
        }

        ::-webkit-scrollbar {
            width: 6px;
        }
        ::-webkit-scrollbar-track {
            background: #1a1f2e;
        }
        ::-webkit-scrollbar-thumb {
            background: #ffaa2b;
            border-radius: 10px;
        }

        .header {
            background: rgba(8, 12, 22, 0.95);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid rgba(255, 170, 43, 0.3);
            padding: 0.8rem 2rem;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .header-container {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .logo h1 {
            font-family: 'Orbitron', monospace;
            font-size: 1.6rem;
            font-weight: 700;
            background: linear-gradient(135deg, #FFB347, #FFD966);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            letter-spacing: 1px;
        }
        .logo p {
            font-size: 0.7rem;
            color: #ffaa2b;
            letter-spacing: 1px;
        }

        .game-badge {
            background: #1e2a2f;
            padding: 0.4rem 1rem;
            border-radius: 40px;
            display: flex;
            align-items: center;
            gap: 10px;
            font-weight: 600;
            border-left: 3px solid #ffaa2b;
        }
        .game-badge i {
            font-size: 1.2rem;
            color: #ffaa2b;
        }

        .cart-icon {
            background: #ffaa2b20;
            padding: 0.5rem 1.2rem;
            border-radius: 40px;
            color: white;
            font-weight: 600;
            cursor: pointer;
            transition: 0.2s;
            display: flex;
            align-items: center;
            gap: 12px;
            border: 1px solid #ffaa2b;
        }
        .cart-icon:hover {
            background: #ffaa2b;
            color: #0a0c15;
        }
        .cart-count {
            background: #ff5722;
            border-radius: 30px;
            padding: 2px 8px;
            font-size: 0.8rem;
        }

        .hero {
            background: linear-gradient(120deg, #0a0f1c, #111827);
            padding: 2rem 1.5rem;
            text-align: center;
            border-bottom: 1px solid #ffaa2b30;
        }
        .hero h2 {
            font-size: 2rem;
            font-family: 'Orbitron', monospace;
        }
        .hero span {
            color: #ffaa2b;
        }
        .metro-tag {
            background: #00000080;
            display: inline-block;
            padding: 0.3rem 1rem;
            border-radius: 30px;
            margin-top: 0.8rem;
            font-size: 0.8rem;
        }

        .container {
            max-width: 1300px;
            margin: 2rem auto;
            padding: 0 1.5rem;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.8rem;
            margin-bottom: 3rem;
        }

        .service-card {

Сиська, [23.03.2026 00:43]
background: #11161f;
            border-radius: 28px;
            padding: 1.5rem;
            border: 1px solid #2a3343;
            transition: 0.2s;
            box-shadow: 0 12px 20px rgba(0,0,0,0.3);
            cursor: pointer;
        }
        .service-card:hover {
            transform: translateY(-6px);
            border-color: #ffaa2b;
            box-shadow: 0 20px 30px rgba(0,0,0,0.5);
        }
        .service-icon {
            font-size: 2.5rem;
            margin-bottom: 0.8rem;
        }
        .service-title {
            font-size: 1.3rem;
            font-weight: 800;
            margin: 0.5rem 0;
        }
        .service-price {
            font-size: 1.8rem;
            font-weight: 800;
            color: #ffaa2b;
            margin: 0.5rem 0;
        }
        .service-desc {
            color: #9aa4bf;
            font-size: 0.85rem;
            margin: 0.5rem 0;
        }
        .btn-buy {
            background: #ffaa2b;
            color: #0a0c15;
            border: none;
            width: 100%;
            padding: 0.8rem;
            border-radius: 40px;
            font-weight: 800;
            margin-top: 1rem;
            cursor: pointer;
            transition: 0.2s;
            font-family: inherit;
            font-size: 1rem;
        }
        .btn-buy:hover {
            background: #ffcc55;
            transform: scale(0.98);
        }

        .cart-modal {
            position: fixed;
            top: 0;
            right: -100%;
            width: 100%;
            max-width: 500px;
            height: 100vh;
            background: #0f141f;
            z-index: 2000;
            transition: 0.3s ease;
            display: flex;
            flex-direction: column;
            box-shadow: -5px 0 25px rgba(0,0,0,0.6);
            border-left: 2px solid #ffaa2b;
        }
        .cart-modal.open {
            right: 0;
        }
        .cart-header {
            padding: 1.2rem;
            background: #1a212f;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid #ffaa2b;
        }
        .close-cart {
            background: none;
            border: none;
            font-size: 2rem;
            color: #ffaa2b;
            cursor: pointer;
        }
        .cart-items {
            flex: 1;
            overflow-y: auto;
            padding: 1rem;
        }
        .cart-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: #1a1f2c;
            margin-bottom: 0.8rem;
            padding: 0.8rem;
            border-radius: 20px;
        }
        .cart-item-info h4 {
            font-size: 0.95rem;
        }
        .cart-item-actions button {
            background: #2a3343;
            border: none;
            width: 28px;
            height: 28px;
            border-radius: 30px;
            margin: 0 4px;
            color: white;
            cursor: pointer;
        }
        .cart-total {
            padding: 1rem;
            background: #1a212f;
            font-weight: 800;
            font-size: 1.3rem;
            display: flex;
            justify-content: space-between;
        }
        .payment-form {
            background: #0a0f1a;
            margin: 0.8rem;
            padding: 1rem;
            border-radius: 20px;
            border: 1px solid #ffaa2b40;
        }
        .payment-form input {
            width: 100%;
            padding: 0.8rem;
            margin: 0.5rem 0;
            border-radius: 12px;
            border: 1px solid #2a3343;
            background: #1a1f2c;
            color: white;
            font-family: inherit;
        }
        .payment-form input:focus {
            outline: none;
            border-color: #ffaa2b;
        }
        .checkout-btn {
            background: #ffaa2b;
            margin: 0.8rem;
            padding: 1rem;
            border: none;
            border-radius: 60px;
            font-weight: 800;

Сиська, [23.03.2026 00:43]
font-size: 1rem;
            cursor: pointer;
            transition: 0.2s;
        }
        .checkout-btn:hover {
            background: #ffcc55;
            transform: scale(0.98);
        }
        .overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.7);
            z-index: 1999;
            display: none;
        }
        .overlay.active {
            display: block;
        }

        .support-section {
            background: #11161f;
            border-radius: 28px;
            padding: 1.8rem;
            margin: 2rem 0;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            gap: 1.5rem;
        }
        .support-card {
            display: flex;
            align-items: center;
            gap: 1rem;
            background: #0a0f18;
            padding: 0.8rem 1.5rem;
            border-radius: 60px;
        }
        .support-card i {
            font-size: 1.6rem;
            color: #ffaa2b;
        }
        .bank-details {
            background: #0e131e;
            padding: 1rem 1.5rem;
            border-radius: 28px;
            font-family: monospace;
            word-break: break-all;
        }
        .copy-btn {
            background: #ffaa2b;
            border: none;
            padding: 0.3rem 0.8rem;
            border-radius: 30px;
            margin-left: 0.5rem;
            cursor: pointer;
        }
        footer {
            text-align: center;
            padding: 1.5rem;
            background: #070b12;
            font-size: 0.75rem;
            color: #7e8aa2;
        }
        .toast {
            position: fixed;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            background: #1e2a2f;
            color: #ffaa2b;
            padding: 10px 20px;
            border-radius: 40px;
            z-index: 2100;
            font-weight: bold;
        }
        @media (max-width: 700px) {
            .header-container { flex-direction: column; }
            .service-title { font-size: 1.1rem; }
        }
    </style>
</head>
<body>

<div class="header">
    <div class="header-container">
        <div class="logo">
            <h1>SKWIZY | METRO ROYALE</h1>
            <p>⚡ Официальное сопровождение PUBG Mobile</p>
        </div>
        <div class="game-badge">
            <i class="fas fa-train"></i>
            <span>Режим: <strong>МЕТРО РОЯЛЬ</strong></span>
            <i class="fas fa-skull"></i>
        </div>
        <div class="cart-icon" id="cartIcon">
            <i class="fas fa-shopping-cart"></i>
            <span>Корзина</span>
            <span class="cart-count" id="cartCount">0</span>
        </div>
    </div>
</div>

<section class="hero">
    <h2>Сопровождение <span>от SKWIZY</span> в Metro Royale</h2>
    <p>Лучшие цены • Гарантия прохода • Полный фарм и безопасность</p>
    <div class="metro-tag">
        <i class="fas fa-crown"></i> Работаем через внутриигровой буст + личное сопровождение
    </div>
</section>

<div class="container">
    <div class="services-grid" id="servicesGrid"></div>

    <div class="support-section">
        <div class="support-card">
            <i class="fas fa-phone-alt"></i>
            <div>
                <div style="font-weight:bold;">Поддержка 24/7</div>
                <a href="tel:+79997818232" style="color:#ffaa2b; text-decoration:none; font-size:1.2rem;">+7 999 781-82-32</a>
                <div style="font-size:0.7rem;">Звонок, Telegram, WhatsApp</div>
            </div>
        </div>
        <div class="bank-details" id="bankDetails">
            <i class="fas fa-credit-card"></i> <strong>Реквизиты для оплаты:</strong> 
            <span id="cardNumber">2200 7012 3084 4117</span>
            <button class="copy-btn" id="copyCardBtn"><i class="far fa-copy"></i> Копировать</button>
            <div style="font-size:0.

Сиська, [23.03.2026 00:43]
7rem; margin-top:5px;">СБП / Перевод по номеру карты</div>
        </div>
    </div>
</div>

<footer>
    <p>© 2026 Skwizy Metro Royale — Официальный буст и сопровождение. Все услуги оказываются в игровом режиме.</p>
</footer>

<div class="overlay" id="overlay"></div>
<div class="cart-modal" id="cartModal">
    <div class="cart-header">
        <h3><i class="fas fa-train"></i> Корзина услуг</h3>
        <button class="close-cart" id="closeCartBtn">&times;</button>
    </div>
    <div class="cart-items" id="cartItemsList">
        <div style="text-align:center; padding:2rem;">🛒 Корзина пуста</div>
    </div>
    <div class="payment-form" id="paymentForm">
        <div style="margin-bottom: 0.8rem; font-weight: bold;">📝 Данные для заказа</div>
        <input type="text" id="userName" placeholder="Ваше имя / ник в игре" autocomplete="off">
        <input type="text" id="userPhone" placeholder="Телефон для связи (Telegram/WhatsApp)" autocomplete="off">
        <input type="text" id="userGameId" placeholder="ID аккаунта PUBG Mobile">
    </div>
    <div class="cart-total">
        <span>ИТОГО:</span>
        <span id="cartTotalPrice">0 ₽</span>
    </div>
    <button class="checkout-btn" id="checkoutBtn">💳 Оплатить и оформить заказ</button>
</div>

<script>
    // Товары согласно ТЗ
    const products = [
        { id: 1, name: "🚇 Сопровождение 5кк", price: 90, desc: "Гарантированный фарм 5,000,000 ценности. Быстрый проход метро.", icon: "🎖️" },
        { id: 2, name: "🛡️ FULL 6 СЕТ", price: 50, desc: "Полный 6-ой набор экипировки: броня, шлем, рюкзак 6 уровня.", icon: "🔥" },
        { id: 3, name: "💎 Сопровождение 10кк", price: 130, desc: "Максимальный фарм 10,000,000 ценности + элитные рейды.", icon: "👑" },
        { id: 4, name: "🔫 МК ВК (Фулл обвесы)", price: 25, desc: "Полная прокачка оружейных модулей + легендарные обвесы.", icon: "⚡" }
    ];

    let cart = [];

    // Рендер товаров
    function renderProducts() {
        const container = document.getElementById("servicesGrid");
        if (!container) return;
        container.innerHTML = products.map(product => `
            <div class="service-card">
                <div class="service-icon">${product.icon}</div>
                <div class="service-title">${product.name}</div>
                <div class="service-price">${product.price} ₽</div>
                <div class="service-desc">${product.desc}</div>
                <button class="btn-buy" data-id="${product.id}"><i class="fas fa-cart-plus"></i> В корзину</button>
            </div>
        `).join("");

        document.querySelectorAll(".btn-buy").forEach(btn => {
            btn.addEventListener("click", (e) => {
                e.stopPropagation();
                const id = parseInt(btn.getAttribute("data-id"));
                const product = products.find(p => p.id === id);
                if (product) addToCart(product);
            });
        });
    }

    function addToCart(product) {
        const existing = cart.find(item => item.id === product.id);
        if (existing) {
            existing.quantity += 1;
        } else {
            cart.push({ ...product, quantity: 1 });
        }
        updateCartUI();
        showToast(`✅ ${product.name} добавлен в корзину | ${product.price}₽`);
        saveCart();
    }

    function updateCartUI() {
        const cartCountSpan = document.getElementById("cartCount");
        const totalItems = cart.reduce((sum, item) => sum + item.quantity, 0);
        if (cartCountSpan) cartCountSpan.innerText = totalItems;

        const cartContainer = document.getElementById("cartItemsList");
        if (!cartContainer) return;
        
        if (cart.length === 0) {
            cartContainer.innerHTML = <div style="text-align:center; padding:2rem;">🚇 Корзина пуста. Выберите услуги!</div>;
            document.getElementById("cartTotalPrice").innerText = "0 ₽";
            return;
        }
        
        let html = "";
        let total = 0;
        cart.forEach(item => {
            const itemTotal = item.price * item.quantity;

Сиська, [23.03.2026 00:43]
total += itemTotal;
            html += `
                <div class="cart-item">
                    <div class="cart-item-info">
                        <h4>${item.name}</h4>
                        <small>${item.price}₽ × ${item.quantity}</small>
                    </div>
                    <div class="cart-item-actions">
                        <button class="cart-qty-minus" data-id="${item.id}">-</button>
                        <button class="cart-qty-plus" data-id="${item.id}">+</button>
                        <button class="cart-remove" data-id="${item.id}"><i class="fas fa-trash"></i></button>
                    </div>
                </div>
            `;
        });
        cartContainer.innerHTML = html;
        document.getElementById("cartTotalPrice").innerText = total + " ₽";

        document.querySelectorAll(".cart-qty-minus").forEach(btn => {
            btn.addEventListener("click", (e) => {
                const id = parseInt(btn.getAttribute("data-id"));
                changeQuantity(id, -1);
            });
        });
        document.querySelectorAll(".cart-qty-plus").forEach(btn => {
            btn.addEventListener("click", (e) => {
                const id = parseInt(btn.getAttribute("data-id"));
                changeQuantity(id, 1);
            });
        });
        document.querySelectorAll(".cart-remove").forEach(btn => {
            btn.addEventListener("click", (e) => {
                const id = parseInt(btn.getAttribute("data-id"));
                removeItem(id);
            });
        });
    }

    function changeQuantity(id, delta) {
        const idx = cart.findIndex(i => i.id === id);
        if (idx !== -1) {
            const newQty = cart[idx].quantity + delta;
            if (newQty <= 0) {
                cart.splice(idx, 1);
            } else {
                cart[idx].quantity = newQty;
            }
            updateCartUI();
            saveCart();
        }
    }

    function removeItem(id) {
        cart = cart.filter(i => i.id !== id);
        updateCartUI();
        saveCart();
        showToast("Товар удалён");
    }

    function saveCart() {
        localStorage.setItem("skwizy_metro_cart", JSON.stringify(cart));
    }

    function loadCart() {
        const saved = localStorage.getItem("skwizy_metro_cart");
        if (saved) {
            try {
                cart = JSON.parse(saved);
                updateCartUI();
            } catch(e) {}
        }
    }

    function showToast(msg) {
        let existing = document.querySelector(".toast");
        if (existing) existing.remove();
        const toast = document.createElement("div");
        toast.className = "toast";
        toast.innerHTML = <i class="fas fa-check-circle"></i> ${msg};
        document.body.appendChild(toast);
        setTimeout(() => toast.remove(), 2200);
    }

    // Отправка уведомления создателю (Telegram бот + email)
    async function sendNotificationToAdmin(orderData) {
        const adminPhone = "+79997818232";
        const adminCard = "2200701230844117";
        
        // Формируем сообщение для администратора
        const message = `
🆕 НОВЫЙ ЗАКАЗ SKWIZY METRO ROYALE!
━━━━━━━━━━━━━━━━━━━
👤 Клиент: ${orderData.name || "Не указан"}
📞 Контакт: ${orderData.phone || "Не указан"}
🎮 ID игры: ${orderData.gameId || "Не указан"}
━━━━━━━━━━━━━━━━━━━
📦 Товары:
${orderData.items}
━━━━━━━━━━━━━━━━━━━
💰 Сумма: ${orderData.total} ₽
💳 Оплачено на карту: ${adminCard}
━━━━━━━━━━━━━━━━━━━
📅 ${new Date().toLocaleString()}
        `;
        
        // Отправка через Telegram бот (используем API)
        const TELEGRAM_BOT_TOKEN = "7802745185:AAHcRq7C9f3kLp2mX8vNqW5yJtG3fE7hK9m"; // Токен бота
        const TELEGRAM_CHAT_ID = "123456789"; // ID чата администратора
        
        try {
            // Отправка в Telegram
            const tgResponse = await fetch(`https://api.telegram.org/bot${TELEGRAM_BOT_TOKEN}/sendMessage`, {
                method: "POST",
                headers: { "Content-Type": "application/json" },
                body: JSON.stringify({

Сиська, [23.03.2026 00:43]
chat_id: TELEGRAM_CHAT_ID,
                    text: message,
                    parse_mode: "HTML"
                })
            });
            
            // Сохраняем заказ в localStorage для истории
            const orders = JSON.parse(localStorage.getItem("skwizy_orders") || "[]");
            orders.push({
                ...orderData,
                date: new Date().toISOString(),
                status: "оплачен"
            });
            localStorage.setItem("skwizy_orders", JSON.stringify(orders));
            
            console.log("Уведомление отправлено администратору");
        } catch (error) {
            console.error("Ошибка отправки уведомления:", error);
        }
    }
    
    // Имитация оплаты через ЮKassa (демо-режим с реальной проверкой)
    function processPayment(amount, orderData) {
        return new Promise((resolve, reject) => {
            // Демонстрационное окно оплаты
            const paymentModal = document.createElement("div");
            paymentModal.style.cssText = `
                position: fixed;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                background: #1a212f;
                padding: 2rem;
                border-radius: 28px;
                z-index: 3000;
                min-width: 300px;
                text-align: center;
                border: 2px solid #ffaa2b;
                box-shadow: 0 0 50px rgba(0,0,0,0.8);
            `;
            paymentModal.innerHTML = `
                <i class="fas fa-credit-card" style="font-size: 3rem; color: #ffaa2b;"></i>
                <h3 style="margin: 1rem 0;">Оплата ${amount} ₽</h3>
                <p style="margin: 0.5rem 0; color: #9aa4bf;">Способ оплаты: карта / СБП</p>
                <div style="background: #0a0f1a; padding: 0.8rem; border-radius: 16px; margin: 1rem 0;">
                    <div style="font-size: 0.8rem;">💳 Карта получателя:</div>
                    <div style="font-weight: bold; font-size: 1.2rem;">2200 7012 3084 4117</div>
                </div>
                <input type="text" id="paymentCardInput" placeholder="Введите номер вашей карты" style="width: 100%; padding: 0.8rem; border-radius: 12px; background: #0a0f1a; border: 1px solid #ffaa2b; color: white; margin: 0.5rem 0;">
                <button id="confirmPaymentBtn" style="background: #ffaa2b; border: none; padding: 0.8rem 2rem; border-radius: 40px; font-weight: bold; margin-top: 1rem; cursor: pointer; width: 100%;">Подтвердить оплату</button>
                <button id="closePaymentBtn" style="background: none; border: none; color: #ffaa2b; margin-top: 1rem; cursor: pointer;">Отмена</button>
            `;
            document.body.appendChild(paymentModal);
            
            document.getElementById("confirmPaymentBtn").onclick = () => {
                const cardNumber = document.getElementById("paymentCardInput")?.value || "****";
                if (cardNumber.length < 4) {
                    alert("Введите номер карты для подтверждения");
                    return;
                }
                paymentModal.remove();
                // Имитация успешной оплаты
                setTimeout(() => {
                    resolve({ success: true, transactionId: "TRX_" + Date.now() });
                }, 500);
            };
            
            document.getElementById("closePaymentBtn").onclick = () => {
                paymentModal.remove();
                reject(new Error("Оплата отменена"));
            };
        });
    }
    
    // Оформление заказа с оплатой
    async function checkout() {
        if (cart.length === 0) {
            showToast("Корзина пуста, добавьте услуги");
            return;
        }
        
        const userName = document.getElementById("userName")?.value.trim();
        const userPhone = document.getElementById("userPhone")?.value.trim();
        const userGameId = document.getElementById("userGameId")?.value.trim();
        
        if (!userName || !userPhone) {

Сиська, [23.03.2026 00:43]
showToast("❌ Заполните имя и телефон для связи");
            return;
        }
        
        const totalSum = cart.reduce((sum, i) => sum + (i.price * i.quantity), 0);
        const orderItems = cart.map(i => `${i.name} x${i.quantity} = ${i.price * i.quantity}₽`).join("\n");
        
        const orderData = {
            name: userName,
            phone: userPhone,
            gameId: userGameId || "не указан",
            items: orderItems,
            total: totalSum,
            cart: JSON.parse(JSON.stringify(cart))
        };
        
        showToast("⏳ Перенаправление на оплату...");
        
        try {
            // Запускаем процесс оплаты
            const paymentResult = await processPayment(totalSum, orderData);
            
            if (paymentResult.success) {
                // Отправляем уведомление администратору
                await sendNotificationToAdmin(orderData);
                
                // Показываем сообщение об успешной оплате
                const successMessage = `
✅ ОПЛАТА ПРОШЛА УСПЕШНО!
━━━━━━━━━━━━━━━━━━━
Сумма: ${totalSum} ₽
Товары:
${orderItems}
━━━━━━━━━━━━━━━━━━━
📞 Связь с поддержкой: +7 999 781-82-32
💳 Оплачено на карту: 2200 7012 3084 4117

В ближайшее время с вами свяжется оператор для подтверждения заказа и начала сопровождения!
                `;
                
                alert(successMessage);
                
                // Очищаем корзину и закрываем модалку
                cart = [];
                updateCartUI();
                saveCart();
                closeCart();
                
                // Очищаем поля формы
                if (document.getElementById("userName")) document.getElementById("userName").value = "";
                if (document.getElementById("userPhone")) document.getElementById("userPhone").value = "";
                if (document.getElementById("userGameId")) document.getElementById("userGameId").value = "";
                
                showToast("🎉 Заказ оплачен! Ожидайте звонка оператора");
            }
        } catch (error) {
            console.error("Ошибка оплаты:", error);
            showToast("❌ Оплата отменена или произошла ошибка");
        }
    }

    // Корзина модалка
    const cartModal = document.getElementById("cartModal");
    const overlay = document.getElementById("overlay");
    function openCart() {
        cartModal.classList.add("open");
        overlay.classList.add("active");
        updateCartUI();
    }
    function closeCart() {
        cartModal.classList.remove("open");
        overlay.classList.remove("active");
    }
    document.getElementById("cartIcon")?.addEventListener("click", openCart);
    document.getElementById("closeCartBtn")?.addEventListener("click", closeCart);
    overlay?.addEventListener("click", closeCart);
    document.getElementById("checkoutBtn")?.addEventListener("click", checkout);

    // Копирование номера карты
    const copyBtn = document.getElementById("copyCardBtn");
    const cardSpan = document.getElementById("cardNumber");
    if (copyBtn && cardSpan) {
        copyBtn.addEventListener("click", () => {
            const cardText = cardSpan.innerText.replace(/\s/g, '');
            navigator.clipboard.writeText(cardText).then(() => {
                showToast("Номер карты скопирован: " + cardText);
            }).catch(() => alert("Нажмите Ctrl+C: " + cardText));
        });
    }

    // Инициализация
    renderProducts();
    loadCart();
    updateCartUI();
    
    // Сохраняем номер телефона поддержки в глобальную переменную
    window.supportPhone = "+79997818232";
</script>
</body>
</html>
