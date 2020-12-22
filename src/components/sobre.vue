<template>
  
  <div id="sobre">
    <h1 class="titletxt">Sobre o ProcuraBooks</h1>
    <br />
    <p class="subtxt">
      O ProcuraBooks é o maior sebo de livros de São Paulo, a mais de dez anos
      no mercado, o ProcuraBooks se destaca pela qualidade de conservação de
      seus livros, pelo abrangente catálogo, preços baixos e pelo atendimento de
      qualidade. <br />
      O catálogo do ProcuraBooks inclui: Livros, Visual Novels, HQs e Mangas dos
      mais diversos gêneros, para clientes frequentes o ProcuraBooks oferece um
      cartão de fidelidade que inclui os seguintes beneficios: Descontos
      especiais, Desconto de 20% na compra de coleções completas, e muito mais!
      Venha visitar nossa loja e encontre os melhores preços de sebo do Brasil!
    </p>

    <v-carousel
      cycle
      height="500"
      hide-delimiter-background
      :show-arrows="isMobile"
      style="z-index: 0">
      <v-carousel-item v-for="(slide, i) in slides" :key="i" :src="slide.src">
          <v-row class="fill-height" align="center" justify="center">
            <h1 class="slideTitle">{{ slide.msg }}</h1>
          </v-row>
      </v-carousel-item>
    </v-carousel>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slides: [
        { msg: "Catálogo com mais de 3 mil livros!", src: require('./img/catalogo.jpeg') },
        { msg: "Espaço reservado para leitura/estudos", src: require('./img/pexels-helena-lopes-3471028.jpg') },
        { msg: "Os melhores preços de sebo no Brasil", src: require('./img/livrocomfundo.jpeg') },
        { msg: "Descontos exclusivos para estudantes", src: require('./img/iStock-487922329_master.jpg') },
        { msg: "Venha redescobrir o prazer em ler", src: require('./img/pexels-photo-3747468.jpeg') },
      ],
      isMobile: ''
    };
  },
  mounted(){
    window.onresize = () => window.innerWidth<=965?this.isMobile=false:this.isMobile=true
    window.onload = () => window.innerWidth<=965?this.isMobile=false:this.isMobile=true
  }
};
</script>

<style scoped>
#sobre {
  margin-top: 45px;
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
.slideTitle {
  font-family: 'Oswald', sans-serif;
  font-size: 38pt;
  background: rgba(0, 0, 0, 0.377);
  padding: 10px;
  border-radius: 5px;
  text-align: center;
}
@media (max-width: 720px) {
  #sobre {
    margin-right: 5%;
    margin-left: 5%;
  }
  .subtxt {
    font-size: 14pt;
  }
  .slideTitle {
    font-size: 32pt;
    width: 100%;
  }
}
</style>