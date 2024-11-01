<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Compramos Oportunidades, SL</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f8f9fa;
            color: #343a40;
        }
        header {
            background: #007bff;
            color: #fff;
            padding: 20px 0;
            text-align: center;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
            position: relative;
        }
        .cart-icon {
            position: absolute;
            right: 20px;
            top: 20px;
            font-size: 1.5em;
            cursor: pointer;
        }
        h1 {
            margin: 0;
            font-size: 2.5em;
        }
        .container {
            max-width: 1200px;
            margin: 20px auto;
            padding: 20px;
            background: #fff;
            border-radius: 8px;
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.1);
        }
        h2 {
            color: #007bff;
            border-bottom: 2px solid #007bff;
            padding-bottom: 10px;
            margin-bottom: 15px;
        }
        .section {
            margin-bottom: 20px;
        }
        .catalog {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
        }
        .catalog-item {
            border: 1px solid #ced4da;
            border-radius: 5px;
            overflow: hidden;
            background-color: #f8f9fa;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .catalog-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
        }
        .catalog-item img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        .catalog-item-content {
            padding: 15px;
        }
        .catalog-item h3 {
            margin: 0;
            color: #343a40;
        }
        .catalog-item p {
            margin: 5px 0;
        }
        footer {
            text-align: center;
            margin-top: 20px;
            font-size: 0.9em;
            color: #6c757d;
            padding: 20px 0;
            background: #f1f1f1;
            border-top: 1px solid #dee2e6;
        }
        .cart-summary {
            display: none;
            position: absolute;
            right: 20px;
            top: 70px;
            background-color: white;
            border: 1px solid #dee2e6;
            border-radius: 5px;
            padding: 10px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
            z-index: 10;
        }
        .roulette {
            margin-left: 20px;
            display: inline-block;
            padding: 20px;
            border: 2px solid #007bff;
            border-radius: 5px;
            cursor: pointer;
            text-align: center;
            background-color: #f8f9fa;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            position: relative;
        }
        .roulette:hover {
            background-color: #e9ecef;
        }
        .roulette p {
            margin: 0;
            font-weight: bold;
        }
        .review-form, .contact-form {
            margin-top: 20px;
            padding: 15px;
            border: 1px solid #ced4da;
            border-radius: 5px;
        }
        .review-form input, .review-form textarea,
        .contact-form input, .contact-form textarea {
            width: 100%;
            margin-bottom: 10px;
            padding: 10px;
            border: 1px solid #ced4da;
            border-radius: 5px;
        }
        .social-icons {
            margin-top: 10px;
        }
        .social-icons a {
            margin: 0 10px;
            font-size: 1.5em;
            color: #007bff;
        }
    </style>
</head>
<body>

<header>
    <h1>Compramos Oportunidades, SL</h1>
    <div class="cart-icon" onclick="toggleCart()">
        <i class="fas fa-shopping-cart"></i> <span id="cart-count">0</span>
    </div>
</header>

<div class="container">
    <div class="section">
        <h2>¿Quiénes Somos y Nuestro Objetivo?</h2>
        <p>En Compramos Oportunidades, SL, nos dedicamos a dar una segunda vida a objetos que merecen ser rescatados. Nuestro objetivo es darle una nueva oportunidad a cualquier tipo de objeto, desde cañas de pescar hasta mesas o camisetas. Nos encargamos de comprarlos, restaurarlos y ponerlos a la venta, valorando la importancia de las segundas oportunidades de los objetos.</p>
    </div>

    <div class="section">
        <h2>Catálogo de Artículos</h2>
        <div class="catalog">
            <div class="catalog-item">
                <img src="https://via.placeholder.com/300x200" alt="Caña de Pescar">
                <div class="catalog-item-content">
                    <h3>Caña de Pescar</h3>
                    <p><strong>Descripción:</strong> Caña de pescar de fibra de carbono, ligera y resistente.</p>
                    <p><strong>Precio:</strong> 35 €</p>
                    <button class="add-to-cart" onclick="addToCart('Caña de Pescar', 35)">Añadir a la Cesta</button>
                </div>
            </div>
            <div class="catalog-item">
                <img src="https://via.placeholder.com/300x200" alt="Mesita de Noche">
                <div class="catalog-item-content">
                    <h3>Mesita de Noche</h3>
                    <p><strong>Descripción:</strong> Mesita de noche de madera reciclada, ideal para cualquier dormitorio.</p>
                    <p><strong>Precio:</strong> 50 €</p>
                    <button class="add-to-cart" onclick="addToCart('Mesita de Noche', 50)">Añadir a la Cesta</button>
                </div>
            </div>
            <div class="catalog-item">
                <img src="https://via.placeholder.com/300x200" alt="Camiseta Vintage">
                <div class="catalog-item-content">
                    <h3>Camiseta Vintage</h3>
                    <p><strong>Descripción:</strong> Camiseta de algodón 100%, estilo retro.</p>
                    <p><strong>Precio:</strong> 20 €</p>
                    <button class="add-to-cart" onclick="addToCart('Camiseta Vintage', 20)">Añadir a la Cesta</button>
                </div>
            </div>
            <div class="catalog-item">
                <img src="https://via.placeholder.com/300x200" alt="Silla de Oficina">
                <div class="catalog-item-content">
                    <h3>Silla de Oficina</h3>
                    <p><strong>Descripción:</strong> Silla de oficina ergonómica, ideal para largas horas de trabajo.</p>
                    <p><strong>Precio:</strong> 70 €</p>
                    <button class="add-to-cart" onclick="addToCart('Silla de Oficina', 70)">Añadir a la Cesta</button>
                </div>
            </div>
            <div class="catalog-item">
                <img src="https://via.placeholder.com/300x200" alt="Lámpara de Mesa">
                <div class="catalog-item-content">
                    <h3>Lámpara de Mesa</h3>
                    <p><strong>Descripción:</strong> Lámpara de mesa vintage con luz LED.</p>
                    <p><strong>Precio:</strong> 25 €</p>
                    <button class="add-to-cart" onclick="addToCart('Lámpara de Mesa', 25)">Añadir a la Cesta</button>
                </div>
            </div>
            <div class="catalog-item">
                <img src="https://via.placeholder.com/300x200" alt="Espejo Decorativo">
                <div class="catalog-item-content">
                    <h3>Espejo Decorativo</h3>
                    <p><strong>Descripción:</strong> Espejo de diseño moderno, ideal para cualquier habitación.</p>
                    <p><strong>Precio:</strong> 40 €</p>
                    <button class="add-to-cart" onclick="addToCart('Espejo Decorativo', 40)">Añadir a la Cesta</button>
                </div>
            </div>
            <div class="catalog-item">
                <img src="https://via.placeholder.com/300x200" alt="Set de Jardinería">
                <div class="catalog-item-content">
                    <h3>Set de Jardinería</h3>
                    <p><strong>Descripción:</strong> Herramientas de jardinería recicladas, perfectas para el jardín.</p>
                    <p><strong>Precio:</strong> 30 €</p>
                    <button class="add-to-cart" onclick="addToCart('Set de Jardinería', 30)">Añadir a la Cesta</button>
                </div>
            </div>
        </div>
    </div>

    <div class="section">
        <h2>Resumen de la Cesta</h2>
        <div class="cart-summary" id="cart-summary">
            <h3>Artículos en la Cesta:</h3>
            <ul id="cart-items"></ul>
            <strong>Total: €<span id="cart-total">0</span></strong>
            <br>
            <button onclick="checkout()">Finalizar Compra</button>
            <div class="roulette" onclick="spinRoulette()">
                <p>¡Gira la Ruleta!</p>
            </div>
        </div>
    </div>

    <div class="review-form">
        <h2>Deja tu Reseña</h2>
        <input type="text" placeholder="Tu Nombre" required>
        <textarea rows="4" placeholder="Escribe tu reseña..." required></textarea>
        <button onclick="submitReview()">Enviar Reseña</button>
    </div>

    <div class="contact-form">
        <h2>Contacto</h2>
        <input type="text" placeholder="Tu Nombre" required>
        <input type="email" placeholder="Tu Correo Electrónico" required>
        <textarea rows="4" placeholder="Tu Mensaje..." required></textarea>
        <button onclick="submitContact()">Enviar Mensaje</button>
    </div>
</div>

<footer>
    <p>&copy; 2024 Compramos Oportunidades, SL. Todos los derechos reservados.</p>
    <div class="social-icons">
        <a href="#"><i class="fab fa-facebook"></i></a>
        <a href="#"><i class="fab fa-instagram"></i></a>
        <a href="#"><i class="fab fa-twitter"></i></a>
    </div>
</footer>

<script>
    let cart = [];
    let cartCount = 0;
    let cartTotal = 0;

    function addToCart(item, price) {
        cart.push({ item, price });
        cartCount++;
        cartTotal += price;
        document.getElementById('cart-count').innerText = cartCount;
        document.getElementById('cart-summary').style.display = 'block';
        updateCart();
    }

    function updateCart() {
        const cartItems = document.getElementById('cart-items');
        cartItems.innerHTML = '';
        cart.forEach((product) => {
            const li = document.createElement('li');
            li.innerText = `${product.item} - €${product.price}`;
            cartItems.appendChild(li);
        });
        document.getElementById('cart-total').innerText = cartTotal.toFixed(2);
    }

    function toggleCart() {
        const summary = document.getElementById('cart-summary');
        summary.style.display = summary.style.display === 'block' ? 'none' : 'block';
    }

    function spinRoulette() {
        const discount = Math.floor(Math.random() * 31); // 0-30% de descuento
        alert(`¡Felicidades! Has ganado un descuento del ${discount}%`);
        applyDiscount(discount);
    }

    function applyDiscount(discount) {
        cartTotal = cart.reduce((total, product) => total + product.price, 0);
        const discountAmount = (cartTotal * discount) / 100;
        const newTotal = cartTotal - discountAmount;
        document.getElementById('cart-total').innerText = newTotal.toFixed(2);
        alert(`Total después del descuento: €${newTotal.toFixed(2)}`);
    }

    function checkout() {
        alert('Gracias por tu compra!');
        cart = [];
        cartCount = 0;
        cartTotal = 0;
        document.getElementById('cart-count').innerText = cartCount;
        document.getElementById('cart-summary').style.display = 'none';
    }

    function submitReview() {
        alert('Gracias por tu reseña!');
    }

    function submitContact() {
        alert('Gracias por tu mensaje!');
    }
</script>

</body>
</html>
