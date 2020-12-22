<template>
  <div id="catalogo">
    <h1 class="titletxt">Nosso Catálogo</h1>
    <br>
    <p class="subtxt">O catálogo do ProcuraBooks inclui obras clássicas as mais recentes, vendemos edições soltas 
      e também coleções completas, nossos preços variam de acordo com o estado de conservação e raridade da edição,
      para informações de disponibilidade de alguma edição nos contate utilizando os dados de contato disponibilazados abaixo
      na aba Onde Estamos/Contato. <br>
      Abaixo você pode conferir algumas das obras mais populares de nosso catálogo.
    </p>
    <h1 class="titletxt" style="text-align: center; border: none; padding-bottom: 15px;">Títulos Populares</h1>
    <div id="livros"> 
      <img v-for="(livro, i) in livros" :key="i" :src="livro" class="livro" width="200">
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      livros: [
        require('./img/1008083074.jpg'),
        require('./img/Rsz_2001.png'),
        require('./img/1008978141.jpg'),
        require('./img/51zhRn-CtUL.jpg'),
        require('./img/672314.jpg'),
        require('./img/81RFAJmHG1L.jpg'),
        require('./img/1006627766.jpg'),
        require('./img/41Imin+TayL.jpg'),
        require('./img/transferir.jpg'),
        require('./img/5115VsJpk3L._SX319_BO1,204,203,200_.jpg'),
        require('./img/51JeIlr1pYL._SX346_BO1,204,203,200_.jpg'),
        require('./img/51dU+s4FLDL._SX346_BO1,204,203,200_.jpg'),
        require('./img/61-2G84LF-L.jpg'),
        require('./img/61fhUR+ubQL.jpg'),
      ]
    }
  }
};
</script>

<style scoped >
#catalogo {
  margin-top: 35px;
  margin-right: 12%;
  margin-left: 12%;
}
.titletxt {
  font-family: "Oswald", sans-serif;
  padding-left: 10px;
  font-size: 28pt;
  border-left: solid 5px;
  border-left-color: #ff8331;
}
.subtxt {
  font-family: "Noto Sans", sans-serif;
  font-size: 15pt;
}

#livros {
 height: 300px;
 display: flex;
 overflow-x: scroll;
}

.livro {padding: 5px 7px;}

::-webkit-scrollbar {
  width: 10px;
}
::-webkit-scrollbar:hover {
  background-image: rgba(0, 0, 0, 0.445);
}
::-webkit-scrollbar-thumb {
  background-color: rgba(153, 153, 153, 0.377);
  border-radius: 10px;
}
::-webkit-scrollbar-thumb:hover {
  background-color: rgba(153, 153, 153, 0.582);
}
::-webkit-scrollbar-thumb:active,
::-webkit-scrollbar-thumb:hover:active {
  background-color: rgba(153, 153, 153, 0.678);
}

@media (max-width: 720px) {
  #catalogo {
    margin-right: 5%;
    margin-left: 5%;
  }
  .subtxt {
    font-size: 14pt;
  }
}
</style>