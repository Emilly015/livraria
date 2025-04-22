<script setup>
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
            <li><span class="fa-solid fa-cart-shopping"> |</span></li>
            <li><span class="fa-solid fa-heart"> |</span></li>
            <li><span class="fa-solid fa-user"> |</span></li>
          </ul>
        </div>
      </nav>
    </header>
    <hr />
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
    <hr />
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
    <hr />
    <section class="lancamento">
      <h1>Lançamentos</h1>
      <div class="primeiros">
      <ul>
      <li>
      <img src="/bela.png" alt="">
      <h4>Chain of Iron: Volume 2</h4>
      <p>Cassandra Clare</p>
      <p>R$23.24</p>
      <button>Comprar</button>
      </li>
      <li>
        <img src="/princesa.png" alt="">
        <h4>Chain of Thorns</h4>
        <p>Cassandra Clare</p>
        <p>R$23.24</p>
        <button>Comprar</button>
      </li>
      <li>
        <img src="/jogo.png" alt="">
        <h4>City of Fallen Angels</h4>
        <p>Cassandra Clare</p>
        <p>R$13.94</p>
        <button>Comprar</button>
      </li>
      <li>
        <img src="/cassandra.png" alt="">
        <h4>Nona the Ninth</h4>
        <p>Cassandra Clare</p>
        <p>R$16.84</p>
        <button>Comprar</button>
      </li>
      </ul>
    </div>
      <div class="segundos">
        <ul>
          <li>
            <img src="/colson.png" alt="">
            <h4>Harlem Shuffle</h4>
            <p>Colson Whitehead</p>
            <p>R$26.92</p>
            <button>Comprar</button>
          </li>
          <li>
            <img src="/montanha.png" alt="">
            <h4>Two Old Women</h4>
            <p>Velma Wallis</p>
            <p>R$13.95</p>
            <button>Comprar</button>
          </li>
          <li>
            <img src="/amarelo.png" alt="">
            <h4>Carrie Soto Is Back</h4>
            <p>Taylor Jenkins Reid</p>
            <p>R$26.04</p>
            <button>Comprar</button>
          </li>
          <li>
            <img src="/azul.png" alt="">
            <h4>Book Lovers</h4>
            <p>Emily Henry</p>
            <p>R$15.81</p>
            <button>Comprar</button>
          </li>
        </ul>
      </div>
   
    </section>
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
header{
  margin: 2vw 0 0.1vw 0;
}
header nav h3{
  margin: 0 5vw 0 0;
}
header div.pesquisa input{
  padding: 10px 40px 10px 10px;
  margin: 1.2vw 0 0 0;
  background-color: #F1F1F1;
  border: none;
}

header div.logo h1{
  margin: 0 0 0 3vw;
}

div.lista {
  margin: 0 5vw 0 0;
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
div.lista li.devo{
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
hr{
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
section.autor div.book button.abril{
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
section.topicos div.icons ul{
  display: flex;
  margin: 0 0 0 5vw;
  list-style: none;
 
}
section.topicos div.icons ul li{
  margin: 0 15vw 0 0;
  font-size: 1.2rem;
  font-weight: bold;
  color: #231F2D;
}
section.topicos div.icons ul li span{
  padding: 0 25px 0 0;
  font-size: 40px;
  color: #231F2D;
}
section.topicos div.icons div.vertical {           
  height: 40px;           
  background-color: black; 
  border-left: 2px solid;
}
div.primeiros{
  display: flex; /*errado*/
}
</style>
