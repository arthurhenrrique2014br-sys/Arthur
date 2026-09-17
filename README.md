<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Pizza Mania 🍕</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        body {
            background: #f5f5f5;
            color: #222;
        }

        /* CABEÇALHO */
        header {
            background: #c62828;
            color: white;
            text-align: center;
            padding: 20px;
        }

        header h1 {
            font-size: 30px;
        }

        header p {
            margin-top: 5px;
        }

        /* BANNER */
        .banner {
            background: #222;
            color: white;
            text-align: center;
            padding: 50px 20px;
        }

        .banner h2 {
            font-size: 32px;
            margin-bottom: 10px;
        }

        .banner p {
            font-size: 18px;
        }

        .botao-cardapio {
            margin-top: 20px;
            padding: 13px 25px;
            border: none;
            border-radius: 8px;
            background: #ffb703;
            font-weight: bold;
            font-size: 16px;
            cursor: pointer;
        }

        /* CONTEÚDO */
        .container {
            max-width: 1000px;
            margin: auto;
            padding: 30px 15px;
        }

        .container > h2 {
            text-align: center;
            margin-bottom: 25px;
        }

        /* PIZZAS */
        .pizzas {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 20px;
        }

        .pizza {
            background: white;
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }

        .pizza-imagem {
            font-size: 65px;
        }

        .pizza h3 {
            margin: 10px 0;
        }

        .pizza p {
            color: #666;
            min-height: 40px;
        }

        .preco {
            display: block;
            color: #c62828;
            font-size: 21px;
            font-weight: bold;
            margin: 15px 0;
        }

        .botao-adicionar {
            background: #c62828;
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 8px;
            font-weight: bold;
            cursor: pointer;
        }

        .botao-adicionar:hover {
            background: #9e1d1d;
        }

        /* CARRINHO */
        .carrinho {
            background: white;
            margin-top: 35px;
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }

        .carrinho h2 {
            margin-bottom: 15px;
        }

        .item-carrinho {
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid #ddd;
            padding: 12px 0;
        }

        .botao-remover {
            background: #333;
            color: white;
            border: none;
            padding: 6px 10px;
            border-radius: 5px;
            cursor: pointer;
        }

        .total {
            font-size: 22px;
            font-weight: bold;
            margin: 20px 0;
        }

        .botao-whatsapp {
            width: 100%;
            background: #25d366;
            color: white;
            border: none;
            padding: 15px;
            border-radius: 8px;
            font-size: 17px;
            font-weight: bold;
            cursor: pointer;
        }

        /* INFORMAÇÕES */
        .informacoes {
            background: #222;
            color: white;
            text-align: center;
            padding: 30px 15px;
        }

        .informacoes p {
            margin-top: 8px;
        }

        /* RODAPÉ */
        footer {
            background: #111;
            color: #aaa;
            text-align: center;
            padding: 15px;
        }

        /* CELULAR */
        @media (max-width: 500px) {

            .banner h2 {
                font-size: 25px;
            }

            header h1 {
                font-size: 25px;
            }

        }
    </style>
</head>

<body>

    <!-- CABEÇALHO -->
    <header>
        <h1>🍕 Pizza Mania</h1>
        <p>A melhor pizza da cidade!</p>
    </header>

    <!-- BANNER -->
    <section class="banner">

        <h2>Pizza quentinha na sua casa 🔥</h2>

        <p>Escolha sua pizza favorita e faça seu pedido.</p>

        <button class="botao-cardapio"
        onclick="document.getElementById('cardapio').scrollIntoView()">

            Ver nosso cardápio

        </button>

    </section>

    <!-- CARDÁPIO -->
    <main class="container" id="cardapio">

        <h2>🍕 Nosso Cardápio</h2>

        <div class="pizzas">

            <!-- PIZZA 1 -->
            <div class="pizza">

                <div class="pizza-imagem">🍕</div>

                <h3>Pizza de Calabresa</h3>

                <p>
                    Molho de tomate, queijo,
                    calabresa e cebola.
                </p>

                <span class="preco">R$ 35,00</span>

                <button class="botao-adicionar"
                onclick="adicionarAoCarrinho('Pizza de Calabresa', 35)">

                    Adicionar ao pedido

                </button>

            </div>

            <!-- PIZZA 2 -->
            <div class="pizza">

                <div class="pizza-imagem">🍕</div>

                <h3>Frango com Catupiry</h3>

                <p>
                    Frango desfiado,
                    queijo e catupiry.
                </p>

                <span class="preco">R$ 40,00</span>

                <button class="botao-adicionar"
                onclick="adicionarAoCarrinho('Frango com Catupiry', 40)">

                    Adicionar ao pedido

                </button>

            </div>

            <!-- PIZZA 3 -->
            <div class="pizza">

                <div class="pizza-imagem">🍕</div>

                <h3>Pizza de Muçarela</h3>

                <p>
                    Molho de tomate
                    e muito queijo.
                </p>

                <span class="preco">R$ 32,00</span>

                <button class="botao-adicionar"
                onclick="adicionarAoCarrinho('Pizza de Muçarela', 32)">

                    Adicionar ao pedido

                </button>

            </div>

            <!-- PIZZA 4 -->
            <div class="pizza">

                <div class="pizza-imagem">🍕</div>

                <h3>Pizza Portuguesa</h3>

                <p>
                    Presunto, queijo,
                    ovo, cebola e azeitona.
                </p>

                <span class="preco">R$ 42,00</span>

                <button class="botao-adicionar"
                onclick="adicionarAoCarrinho('Pizza Portuguesa', 42)">

                    Adicionar ao pedido

                </button>

            </div>

            <!-- PIZZA 5 -->
            <div class="pizza">

                <div class="pizza-imagem">🍕</div>

                <h3>Pizza 4 Queijos</h3>

                <p>
                    Muçarela, parmesão,
                    provolone e catupiry.
                </p>

                <span class="preco">R$ 45,00</span>

                <button class="botao-adicionar"
                onclick="adicionarAoCarrinho('Pizza 4 Queijos', 45)">

                    Adicionar ao pedido

                </button>

            </div>

            <!-- PIZZA 6 -->
            <div class="pizza">

                <div class="pizza-imagem">🍕</div>

                <h3>Pizza de Chocolate</h3>

                <p>
                    Uma deliciosa pizza
                    doce de chocolate.
                </p>

                <span class="preco">R$ 38,00</span>

                <button class="botao-adicionar"
                onclick="adicionarAoCarrinho('Pizza de Chocolate', 38)">

                    Adicionar ao pedido

                </button>

            </div>

        </div>

        <!-- CARRINHO -->
        <section class="carrinho">

            <h2>🛒 Seu Pedido</h2>

            <div id="listaCarrinho">
                <p>Seu pedido está vazio.</p>
            </div>

            <div class="total">
                Total: R$ <span id="total">0,00</span>
            </div>

            <button class="botao-whatsapp"
            onclick="enviarPedido()">

                📲 Fazer pedido pelo WhatsApp

            </button>

        </section>

    </main>

    <!-- INFORMAÇÕES -->
    <section class="informacoes">

        <h2>📍 Pizza Mania</h2>

        <p>Rua das Pizzas, nº 123</p>

        <p>📞 (00) 00000-0000</p>

        <p>🕐 Funcionamento: 18h às 23h</p>

    </section>

    <!-- RODAPÉ -->
    <footer>

        © 2026 Pizza Mania - Todos os direitos reservados.

    </footer>


    <script>

        // Carrinho
        let carrinho = [];


        // Adicionar pizza
        function adicionarAoCarrinho(nome, preco) {

            carrinho.push({
                nome: nome,
                preco: preco
            });

            atualizarCarrinho();

            alert(nome + " foi adicionado ao seu pedido! 🍕");

        }


        // Remover pizza
        function removerDoCarrinho(indice) {

            carrinho.splice(indice, 1);

            atualizarCarrinho();

        }


        // Atualizar carrinho
        function atualizarCarrinho() {

            const lista = document.getElementById("listaCarrinho");

            const totalElemento = document.getElementById("total");

            lista.innerHTML = "";

            if (carrinho.length === 0) {

                lista.innerHTML =
                    "<p>Seu pedido está vazio.</p>";

                totalElemento.textContent = "0,00";

                return;

            }


            let total = 0;


            carrinho.forEach(function(item, indice) {

                total += item.preco;


                const div = document.createElement("div");

                div.className = "item-carrinho";


                div.innerHTML = `

                    <span>
                        ${item.nome} -
                        R$ ${item.preco.toFixed(2).replace(".", ",")}
                    </span>

                    <button
                        class="botao-remover"
                        onclick="removerDoCarrinho(${indice})">

                        Remover

                    </button>

                `;


                lista.appendChild(div);

            });


            totalElemento.textContent =
                total.toFixed(2).replace(".", ",");

        }


        // Enviar pedido pelo WhatsApp
        function enviarPedido() {

            if (carrinho.length === 0) {

                alert(
                    "Adicione alguma pizza ao seu pedido primeiro! 🍕"
                );

                return;

            }


            let mensagem =
                "🍕 *NOVO PEDIDO - PIZZA MANIA*%0A%0A";


            let total = 0;


            carrinho.forEach(function(item) {

                mensagem +=
                    "🍕 " +
                    item.nome +
                    " - R$ " +
                    item.preco.toFixed(2).replace(".", ",") +
                    "%0A";

                total += item.preco;

            });


            mensagem +=
                "%0A💰 *Total: R$ " +
                total.toFixed(2).replace(".", ",") +
                "*";


            /*
                COLOQUE AQUI O NÚMERO DO WHATSAPP
                DA PIZZARIA.

                Exemplo:
                5565999999999

                55 = Brasil
                65 = Mato Grosso
            */

            const numeroWhatsApp = "5565999999999";


            const link =
                "https://wa.me/" +
                numeroWhatsApp +
                "?text=" +
                mensagem;


            window.open(link, "_blank");

        }

    </script>

</body>
</html>
