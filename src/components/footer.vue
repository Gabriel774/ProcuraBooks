<template>
  <div id="content">
    <div style="margin-top: 20px;">
        <p class="titletxt">Redes Sociais</p>
        <img v-for="(rede,i) in redes" :key="i"  :src="rede" style="width: 50px; margin: 10px; cursor: pointer;">
    </div>
    <p class="subtxt">
        SAC - contato@procurabooks.com.br <br>
        &copy;ProcuraBooks
    </p>
  </div>
</template>

<script>
export default {
    data() {
        return {
            redes: [
                require('./img/twitter.png'),
                require('./img/facebook.png'),
                require('./img/instagram.png'),
                require('./img/youtube.png'),
                require('./img/linkedin.png')
            ]
        }
    }
};
</script>

<style scoped>
#content {
  background: rgb(27, 27, 27);
  color: white;
  margin-top: 30px;
  text-align: center;
}
.titletxt {
  font-family: "Oswald", sans-serif;
  padding-left: 10px;
  font-size: 28pt;
}
.subtxt {
  font-family: "Noto Sans", sans-serif;
  font-size: 15pt;
  text-align: center;
  padding: 20px 0px;
}
@media (max-width: 720px) {
  .subtxt {
    font-size: 14pt;
  }
}
</style>