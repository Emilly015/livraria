<script setup>
import { ref, computed } from 'vue'

const mostrarCarrinho = ref(true)

function abrirCarrinho() {
  mostrarCarrinho.value = true
}
function voltarhome() {
  mostrarCarrinho.value = false
}
const contador = ref(1)
const preco = 23.24
const total = computed(() => {
  return (preco * contador.value).toFixed(2).replace(`.`, `,`)
})
function incrementar() {
  contador.value++
}
function decrementar() {
  contador.value--
}
</script>
<template>

  <body>
    <header>
      <nav>
        <div class="logo">
          <h1><img src="/IFbooks.png" alt=""></h1>
          <h2><img src="/line1.png" alt=""></h2>
          <h3><img src="/aprecologo.png" alt=""></h3>
        </div>
        <div class="pesquisa">
          <input type="" placeholder="Pesquisar">
        </div>
        <div class="lista">
          <ul>
            <li><a href="#">Termos</a></li>
            <li><a href="#">Equipe</a></li>
            <li><a href="#">Envio</a></li>
            <li class="devo"><a href="#">Devoluções</a></li>
          </ul>
        </div>
        <div class="icones">
          <ul>
            <li @click="abrirCarrinho"><span class="fa-solid fa-cart-shopping"> |</span></li>
            <li><span class="fa-solid fa-heart"> |</span></li>
            <li><span class="fa-solid fa-user"> |</span></li>
          </ul>
        </div>
      </nav>
    </header>
    <div class="linha"></div>
    <main v-if="!mostrarCarrinho">
      <section class="autor">
        <div class="book">
          <div>
            <button class="abril">Autor de Abril</button>
            <h1>Eric-Emanuel Schmitt</h1>
            <p>Eric-Emmanuel Schmitt has been awarded more than 20 literary prizes and distinctions, and in 2001 he
              received
              the title of Chevalier des Arts et des Lettres. His books have been translated into over 40 languages.</p>
            <button class="quadrado">Acessar página do livro</button>
          </div>
          <div>
            <img src="/book.png" alt="">
          </div>
        </div>
      </section>
      <div class="linha"></div>
      <section class="topicos">
        <div class="icons">
          <ul>
            <li><span class="fa-solid fa-truck"></span>Frete Grátis para SC</li>
            <div class="vertical"></div>
            <li><span class="fa-solid fa-star"></span>Livros recomendados</li>
            <div class="vertical"></div>
            <li><span class="fa-solid fa-book-open"></span>Mais vendidos</li>
          </ul>
        </div>
      </section>
      <div class="linha"></div>
      <section class="lancamento">
        <h1>Lançamentos</h1>
        <div class="livros">
          <div class="primeiros">
            <ul>
              <li>
                <img src="/bela.png" alt="">
                <h4>Chain of Iron: Volume 2</h4>
                <p>Cassandra Clare</p>
                <p class="preco">R$23.24</p>
                <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
              </li>
              <li>
                <img src="/princesa.png" alt="">
                <h4>Chain of Thorns</h4>
                <p>Cassandra Clare</p>
                <p class="preco">R$23.24</p>
                <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
              </li>
              <li>
                <img src="/jogo.png" alt="">
                <h4>City of Fallen Angels</h4>
                <p>Cassandra Clare</p>
                <p class="preco">R$13.94</p>
                <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
              </li>
              <li>
                <img src="/cassandra.png" alt="">
                <h4>Nona the Ninth</h4>
                <p>Cassandra Clare</p>
                <p class="preco">R$16.84</p>
                <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
              </li>
            </ul>
          </div>
          <div class="segundos">
            <ul>
              <li>
                <img src="/colson.png" alt="">
                <h4>Harlem Shuffle</h4>
                <p>Colson Whitehead</p>
                <p class="preco">R$26.92</p>
                <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
              </li>
              <li>
                <img src="/montanha.png" alt="">
                <h4>Two Old Women</h4>
                <p>Velma Wallis</p>
                <p class="preco">R$13.95</p>
                <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
              </li>
              <li>
                <img src="/amarelo.png" alt="">
                <h4>Carrie Soto Is Back</h4>
                <p>Taylor Jenkins Reid</p>
                <p class="preco">R$26.04</p>
                <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
              </li>
              <li>
                <img src="/azul.png" alt="">
                <h4>Book Lovers</h4>
                <p>Emily Henry</p>
                <p class="preco">R$15.81</p>
                <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
              </li>
            </ul>
          </div>
        </div>
      </section>
    </main>
    <section class="v-else" v-else>
      <h4>Carrinho</h4>
      <div class="titulos">
        <ul>
          <li class="titulo1">Título</li>
          <li>Quantidade</li>
          <li class="sub">Subtotal</li>
        </ul>
      </div>
      <div class="linha"></div>
      <div class="livrinhos1">
        <div>
          <img src="/livrinho.png" alt="" width="94px" height="142px">
        </div>
        <div class="text">
          <h5>Chain of Iron: Volume 2</h5>
          <p>Cassandra Clare</p>
          <p>R$23.24</p>
        </div>
        <div class="boto">
          <div class="botao">
            <button v-on:click="incrementar">+</button>
            <p>{{ contador }}</p>
            <button @click="decrementar">-</button>
          </div>
          <p class="precoTotal"> R${{ total }}</p>
        </div>
      </div>
      <div class="linha2"></div>
      <div class="livrinhos2">
        <div>
          <img src="/livrinho.png" alt="" width="94px" height="142px">
        </div>
        <div class="text">
          <h5>Chain of Iron: Volume 2</h5>
          <p>Cassandra Clare</p>
          <p>R$23.24</p>
        </div>
        <div class="boto">
          <div class="botao">
            <button v-on:click="incrementar">+</button>
            <p>{{ contador }}</p>
            <button @click="decrementar">-</button>
          </div>
          <p class="precoTotal"> R${{ total }}</p>
        </div>
      </div>
      <div class="linha2"></div>
      <button class="voltarhome" @click="voltarhome">Voltar para loja</button>
      <div class="inserirflex">
        <div class="cupom">
        <input type="" placeholder="Código do cupom">
      </div>
      <div class="final">
      <div><button class="inserir"> Inserir Cupom</button></div>
      </div>
      <div class="tabela">
        <h5>Total da compra</h5>
        <div class="espaco">
           <p class="b">Produtos:</p>
          <p>R$175</p>
        </div>
        <div class="linha2"></div>
        <div class="espaco">
          <p class="b">Frete:</p>
          <p>Grátis</p>
        </div>
        <div class="linha2"></div>
        <div class="espaco">
           <p class="b">Total:</p>
           <p>R$175</p>
        </div>
        <button>Ir para o pagamento</button>
      </div>
    </div>
    </section>
    <footer>
      <div class="footer">
        <div class="redes">
          <h3>IFbooks</h3>
          <ul>
            <span class="fa-brands fa-square-facebook"></span>
            <span class="fa-brands fa-square-instagram"></span>
            <span class="fa-brands fa-square-twitter"></span>
          </ul>
        </div>
        <div class="direita">
          <p>Contato</p>
          <ul>
            <li> <span class="fa-solid fa-phone"></span>+55 47 40045263</li>
            <li> <span class="fa-solid fa-clock"></span>8h às 23h - Seg a Sex</li>
            <li> <span class="fa-solid fa-envelope"></span>contato@ifbooks.com</li>
          </ul>
          <div class="cartao">
            <ul>
              <li>
                <img src="/paipal 1.png" alt="">
              </li>
              <li>
                <img src="/MasterCard-Logo-1979 1.png" alt="">
              </li>
              <li>
                <img src="/VISA-card-logo- 1.png" alt="">
              </li>
            </ul>
          </div>
        </div>
      </div>
      <p class="direitos">© Alguns direitos reservados. IFbooks 2025. </p>
    </footer>
  </body>
</template>
<style scoped>
.logo {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

img {
  margin-right: 10px;
}

nav {
  display: flex;
}

header {
  margin: 2vw 0 0.1vw 0;
}

header nav h3 {
  margin: 0 5vw 0 0;
}

header div.pesquisa input {
  padding: 10px 40px 10px 10px;
  margin: 1.2vw 0 0 0;
  background-color: #F1F1F1;
  border: none;
}

header div.logo h1 {
  margin: 0 0 0 3vw;
}

div.lista {
  margin: 0 20vw 0 0;
}

div.lista a {
  text-decoration: none;
  color: black;
}

div.lista ul {
  display: flex;
}

div.lista ul li {
  list-style: none;
  padding: 10px;
}

div.linha {
  border-top: 1px solid #27AE60;
}

div.linha2 {
  border-top: 1px solid rgb(53, 53, 53);
}

div.lista li.devo {
  margin: 0 16vw 0 0;
}

div.icones ul {
  display: flex;
  color: #27AE60;
  list-style: none;
}

div.icones ul li {
  margin: 0 10px 0 0;
}

hr {
  border: 0;
  border-top: 1px solid #27AE60;
}

section.autor {
  margin: 10vw 13vw 0 7vw;
}

section.autor h1 {
  font-weight: bold;
  font-size: 3rem;
}

section.autor button.quadrado {
  padding: 20px;
}

section.autor div.book button.abril {
  padding: 10px;
  border-color: #27AE60;
  background-color: white;
  color: #27AE60;
  border-radius: 0.5cap;
}

div.book {
  display: flex;
}

section.autor button.quadrado {
  border-radius: 0;
  background-color: #27AE60;
  border: none;
  color: white;
  font-weight: bold;

}

section.topicos div.icons ul {
  display: flex;
  margin: 0 0 0 5vw;
  list-style: none;

}

section.topicos div.icons ul li {
  margin: 0 15vw 0 0;
  font-size: 1.2rem;
  font-weight: bold;
  color: #231F2D;
}

section.topicos div.icons ul li span {
  padding: 0 25px 0 0;
  font-size: 40px;
  color: #231F2D;
}

section.topicos div.icons div.vertical {
  height: 40px;
  background-color: black;
  border-left: 2px solid;
}

div.primeiros ul {
  display: flex;
}

div.primeiros ul li {
  margin: 0 2vw 0 5vw;
  list-style: none;
}

div.segundos ul {
  display: flex;
}

div.segundos ul li {
  margin: 0 2vw 0 5vw;
  list-style: none;
}

section.lancamento h1 {
  margin: 4vw 0 3vw 7vw;
  font-size: 2rem;
}

section.lancamento div.livros ul li h4 {
  font-size: 1.2rem;
}

section.lancamento div.livros ul li p.preco {
  font-weight: bold;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  font-size: 1.2rem;
  color: black;
}

section.lancamento div.livros ul li p {
  color: #4F4C57;
}

section.lancamento div.livros ul li button {
  padding: 1vw 5vw 1vw 5vw;
  background-color: #27AE60;
  color: white;
  border: none;
  font-size: 1rem;
}

section.lancamento div.livros ul li button span {
  margin: 0 5px 0 0;
  font-size: 1rem;
}

section.v-else {
  margin: 10vw 0 0 5vw;
}

section.v-else h4 {
  color: #27AE60;
  font-size: 2rem;
  font-weight: bold;
}

section.v-else button.voltarhome {
  border: 1.7px solid black;
  background: white;
  padding: 20px 50px 20px 50px;
  font-size: 1rem;
  font-weight: 500;
  margin: 2.5vw 0 0 1vw;
  border-radius: 4px;

}

section.v-else div.cupom input {
  border: 1.7px solid black;
  background: white;
  padding: 20px 50px 20px 50px;
  font-size: 1rem;
  font-weight: 500;
  margin: 2.5vw 0 0 1vw;
  border-radius: 4px;

}

section.v-else button.inserir {
  border: 1.7px solid white;
  background: #27AE60;
  padding: 20px 50px 20px 50px;
  font-size: 1rem;
  font-weight: 500;
  margin: 2.5vw 0 0 1vw;
  border-radius: 4px;
  color: white;
}
section.v-else div.tabela{
  border: 2px solid gray;
  background: white;
  width: 470px;
  height: 324px;
  top: 1079px;
  left: 841px;
  border-radius: 4px;
  font-size: 1rem;
  font-weight: 500;
  margin: 2.4vw 0 0 25vw;
  padding: 0 0 0 10px;
  
}
section.v-else div.tabela button{
  padding: 20px 50px 20px 50px;
  background-color: #27AE60;
  border-radius: 4px;
  color: white;
  border: 1.7px solid white;
  font-size: 1rem;
  font-weight: 500;
  margin: 0 0 0 100px;
}
section.v-else div.tabela div.espaco{
  display: flex;
}
section.v-else div.tabela div.espaco p.b{
  margin: 0 17vw 0 0;
}
section.v-else div.tabela h5{
  font-size: 1.3rem;
}
section.v-else div.final{
  display: flex;
}
section.v-else div.inserirflex{
  display: flex;
}

section.v-else div.titulos ul {
  display: flex;
  list-style: none;
  color: black;
}

section.v-else div.titulos ul li {
  font-size: 1.3rem;
}

section.v-else div.titulos li.titulo1 {
  margin: 0 50vw 0 0;
  color: black;
}

section.v-else div.titulos li.sub {
  margin: 0 0 0 14vw;
}

section.v-else div.livrinhos1 {
  display: flex;
}

section.v-else div.livrinhos1 div.text {
  margin: 1vw 1vw 0 0;
}

section.v-else div.livrinhos2 div.text {
  margin: 1vw 1vw 0 0;
}

section.v-else div.boto {
  display: flex;
  align-items: center;
  margin: 0 0 0 35.5vw;
}

section.v-else div.boto div.botao {
  display: flex;
  border: 1px solid black;
  padding: 0vw 1.4vw 0vw 1.4vw;
}

section.v-else div.boto button {
  background: white;
  border: none;
}

section.v-else div.boto p.precoTotal {
  margin: 0 0 0 17vw;
  color: #382C2C;
}

section.v-else div.livrinhos1 img {
  margin: 2vw 3vw 2vw 2vw;
}

section.v-else div.livrinhos2 {
  display: flex;
}

section.v-else div.livrinhos2 img {
  margin: 2vw 3vw 2vw 2vw;
}

footer {
  background: #27AE60;
  height: 20vw;
  margin: 12vw 0 0 0;
  color: white;
}

footer h3 {
  color: white;
  font-size: 1rem;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  padding: 2vw 0 0 2vw;
}

footer span {
  color: white;
  font-size: 2rem;
  margin: 0 1vw 0 0;
}

footer div.redes {
  margin: 0 0 0 5vw;
}

footer p ul li span {
  font-size: 0.5rem;
}

footer div.footer {
  display: flex;
}

footer div.footer div.direita {
  margin: 0 0 0 65vw;
}

footer div.footer div.direita ul {
  list-style: none;
}

footer div.footer div.direita ul li {
  padding: 0 0 15px 0;
}

footer div.footer div.direita ul li span {
  font-size: 1rem;
}

footer div.footer div.cartao ul {
  display: flex;
  list-style: none;
}

div.direita p {
  margin: 2vw;
}

footer p.direitos {
  margin: 2vw;
  font-weight: bolder;
  text-align: center;
  border-top: 2px solid #FFFFFF;
  margin-top: 30px;
  padding-top: 15px;
  font-size: 0.9rem;
  color: #F1F1F1;
}
</style>
