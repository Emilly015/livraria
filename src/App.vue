<script setup>
</script>
<template>

  <body>
    <header>
      <nav>
        <div class="logo">
          <h1><img src="/IFbooks.png" alt=""></h1>
          <h2><img src="/aprecologo.png" alt=""></h2>
        </div>
        <input type="text" name="pesquisa" id="pesquisa" required>
        <button>pesquisa</button>
        <div class="lista">
          <ul>
            <li><a href="#">Termos</a></li>
            <li><a href="#">Equipe</a></li>
            <li><a href="#">Envio</a></li>
            <li><a href="#">Devoluções</a></li>
          </ul>
        </div>
        <div class="icones">
          <ul>
            <li><span class="fa-solid fa-cart-shopping"></span></li>
            <li><span class="fa-solid fa-heart"></span></li>
            <li><span class="fa-solid fa-user"></span></li>
          </ul>
        </div>
      </nav>
    </header>
    <section class="autor">
      <div class="book">
        <div>
          <p>Autor de Abril</p>
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
    <section class="topicos">
      <p>Frete Grátis para SC</p>
      <p>Livros recomendados</p>
      <p>Mais vendidos</p>
      

    </section>
  </body>
</template>



<style scoped>
.logo {
  display: flex;
  ;
  align-items: center;
  margin-right: 10px;
}

img {
  margin-right: 10px;
}

nav {
  display: flex;
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

div.icones ul {
  display: flex;
  color: #27AE60;
  list-style: none;
}

div.icones ul li {
  padding: 10px;
}

section.autor {
  margin: 0 13vw 0 7vw;
}

section.autor h1 {
  font-weight: bold;
  font-size: 3rem;
}

section.autor button {
  padding: 20px;
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
</style>
