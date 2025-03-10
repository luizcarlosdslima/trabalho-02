<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Loja Online</title>
    <style>
        /* Estilizando o fundo da página */
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            color: #333;
            margin: 0;
            padding: 0;
            display: flex;
        }

        /* Estilizando o cabeçalho */
        header {
            background-color: #0e12e4;
            color: white;
            padding: 10px 5sssssspx;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            z-index: 1000;
        }

        .store-name span {
            color: #ffcc00;
        }

        .cart {
            font-size: 1.5rem;
            background: white;
            color: #0a0df5;
            padding: 5px 15px;
            border-radius: 20px;
        }

        /* Layout principal */
        .container {
            display: flex;
            width: 100%;
            margin-top: 70px;
        }

        /* Barra lateral */
        .sidebar {
            width: 250px;
            background: white;
            padding: 45px;
            box-shadow: 2px 0 5px rgba(0, 0, 0, 0.1);
            height: 100vh;
            position: fixed;
            left: 0;
            top: 70px;
        }

        .sidebar h2 {
            font-size: 1.2rem;
            margin-bottom: 10px;
        }

        .sidebar ul {
            list-style: none;
            padding: 0;
        }

        .sidebar ul li {
            padding: 10px 0;
            border-bottom: 1px solid #ddd;
        }

        .sidebar ul li a {
            text-decoration: none;
            color: #333;
            display: block;
        }

        .sidebar ul li a:hover {
            color: #0a0df5;
        }

        /* Seção de produtos */
        .content {
            flex: 1;
            padding: 20px;
            margin-left: 270px;
        }

        .products {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
        }

        /* Estilizando os produtos */
        .product {
            background: white;
            padding: 15px;
            border-radius: 10px;
            box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        /* Ajustando tamanho das imagens */
        .product img {
            width: 100%;
            height: auto;
            max-width: 150px;
            display: block;
            margin: 0 auto;
        }

        /* Estilizando os preços */
        .price {
            font-size: 1.2rem;
            font-weight: bold;
        }

        .price span {
            color: green;
        }

        /* Botão de adicionar ao carrinho */
        button {
            background-color: #095fcf;
            color: white;
            border: none;
            padding: 10px;
            font-size: 1rem;
            cursor: pointer;
            border-radius: 40px;
        }

        button:hover {
            background-color: #144ae0;
        }
    </style>
</head>
<body>
    <header>
        <h1 class="store-name">Loja <span> Virtual Trabalho</span></h1>
        <div class="cart">
        🛒 <span id="cart-count">0</span>
        </div>
    </header>

    <div class="container">
        <!-- Barra Lateral -->
        <nav class="sidebar">
            
            
            
            <h2> Categorias </h2>
            <ul>
                <li><a href="#">Eletrônicos</a></li>
                <li><a href="#">Eletrodomésticos</a></li>
                <li><a href="#">Smartphones</a></li>
                <li><a href="#">Informática</a></li>
                <li><a href="#">Acessórios</a></li>
            </ul>
        </nav>

        <!-- Seção de Produtos -->
        <div class="content">
            <section class="products">
                <div class="product">
                    <img src="https://m.media-amazon.com/images/I/61KmVBD4ZfL.AC_SX679.jpg" alt="Produto 1">
                    <h2 class="product-name">Fone de Ouvido JBL</h2>
                    <p class="price">-6% <span>R$170,28</span></p>
                    <button onclick="addToCart()">Adicionar ao Carrinho</button>
                </div>
                
                <div class="product">
                    <img src="https://m.media-amazon.com/images/I/51Q85naBNDL.AC_SX679.jpg" alt="Produto 2">
                    <h2 class="product-name">Ventilador de Mesa Mondial</h2>
                    <p class="price"><span>R$114,90</span></p>
                    <button onclick="addToCart()">Adicionar ao Carrinho</button>
                </div>

                <div class="product">
                    <img src="https://m.media-amazon.com/images/I/61ClMfyPd+L.AC_SY300_SX300.jpg" alt="Produto 3">
                    <h2 class="product-name">Smart TV Philips 43"</h2>
                    <p class="price"><span>R$1.599,00</span></p>
                    <button onclick="addToCart()">Adicionar ao Carrinho</button>
                </div>

                <div class="product">
                    <img src="https://m.media-amazon.com/images/I/61zzNZRM-FL.AC_SX679.jpg" alt="Produto 4">
                    <h2 class="product-name">Ar-condicionado Samsung</h2>
                    <p class="price">-10% <span>R$4.499,10</span></p>
                    <button onclick="addToCart()">Adicionar ao Carrinho</button>
                </div>
            </section>
        </div>
    </div>

    <script>
        let cartCount = 0;

        function addToCart() {
            cartCount++;
            document.getElementById("cart-count").innerText = cartCount;
        }
    </script>
</body>
</html>


