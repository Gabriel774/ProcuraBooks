<template>
  <div id="funcionarios">
    <h1 class="titletxt">Funcionários</h1>
    <br>
    <p class="subtxt">A equipe do ProcuraBooks é formada por profissionais extremamente
      capacitados para atende-lo da melhor forma possível.
    </p>
    <br>
    <div id="cards">
      <v-card elevation="2" class="card" shaped v-for="(funcinario, i) in funcionarios" :key="i">
        <div class="profile">
          <img :src="funcinario.src" style="height: 150px; border-radius: 50%;">
          <h1>{{ funcinario.nome }}</h1>
        </div>
        <div class="cargo"> <h2>{{ funcinario.cargo }}</h2></div>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      funcionarios:[
        {src: require('./img/homem-1.png'), nome: "João Jossoares", cargo: 'CEO ProcuraBooks'},
        {src: require('./img/homem-2.png'), nome: "Pedro Santana", cargo: 'CFO ProcuraBooks'},
        {src: require('./img/mulher-1.png'), nome: "Ana Takamaki", cargo: 'Gerente'},
        {src: require('./img/mulher-2.png'), nome: "Tamara Alves", cargo: 'Chefe RH'},
        {src: require('./img/homem-3.png'), nome: "Heitor Castro", cargo: 'Funcinário RH'},
        {src: require('./img/mulher-3.png'), nome: "Leticia Cardoso", cargo: 'Atendente'},
        {src: require('./img/mulher-4.png'), nome: "Luana Alves", cargo: 'Atendente'},
        {src: require('./img/homem-4.png'), nome: "Hugo Augusto", cargo: 'Atendente'},
        {src: require('./img/homem-5.png'), nome: "Henrique Silva", cargo: 'Atendente'},
        {src: require('./img/mulher-5.png'), nome: "Carla Rosa", cargo: 'Atendente'}
      ]
    }
  }
};
</script>

<style scoped>
#funcionarios {
  margin-top: 35px;
  margin-right: 12%;
  margin-left: 12%;
}
#cards {
  display: flex;
  flex-wrap: wrap;
  text-align: center;
  justify-content: space-around;
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
.card {
  width: 290px;
  padding: 30px;
  margin-bottom: 30px;
}
@media (max-width: 720px) {
  #funcionarios {
    margin-right: 5%;
    margin-left: 5%;
  }
  .subtxt {
    font-size: 14pt;
  }
}
</style>