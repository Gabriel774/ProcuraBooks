<template>
  <v-app>
    <app-parallax />
    <app-sobre />
    <hr />
    <app-catalogo />
    <hr />
    <app-funcionarios />
    <hr />
    <app-contato />
    <app-footer />
    <app-header />
  </v-app>
</template>

<script>
import parallax from "./components/parallax";
import header from "./components/header";
import sobre from "./components/sobre";
import catalogo from "./components/catalogo";
import funcionarios from "./components/funcinarios";
import contato from "./components/contato"
import footer from "./components/footer"
export default {
  name: "App",
  components: {
    appHeader: header,
    appParallax: parallax,
    appSobre: sobre,
    appCatalogo: catalogo,
    appFuncionarios: funcionarios,
    appContato: contato,
    appFooter: footer
  },
};
</script>

<style scoped>
hr {
  margin-top: 45px;
  margin-right: 15%;
  margin-left: 15%;
}
@media (max-width: 720px) {
  hr {
    margin-right: 10%;
    margin-left: 10%;
  }
}
</style>