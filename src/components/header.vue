<template>
  <div>
    <div
      style="position: fixed; top: 0px; right: 0px; left: 0px"
      :class="{ color: !headerFade, transparent: headerFade }"
    >
      <img
        src="./img/logo-transparente-branca.png"
        v-if="headerFade"
        id="logo"
      />
      <img
        src="./img/logo-transparente.png"
        v-else
        id="logo"
        @click="$vuetify.goTo('#inicio')"
      />
      <img src="./img/livro-branco.png" v-if="headerFade" id="logoMobile" />
      <img
        src="./img/livro.png"
        v-else
        id="logoMobile"
        @click="$vuetify.goTo('#inicio')"
      />
      <div id="links">
        <h2 v-for="link in links" :key="link.href">
          <a
            class="menu"
            @click="$vuetify.goTo(link.href)"
            :class="{ menuwhite: headerFade, menublack: !headerFade }"
            >{{ link.nome }}</a
          >
        </h2>
      </div>
      <div id="hamburguer">
        <v-app-bar-nav-icon v-if="!headerFade" @click="drawer = !drawer" />
        <v-app-bar-nav-icon v-else dark @click="drawer = !drawer" />
      </div>

      <div class="drawer" :class="{ show: drawer }">
        <div style="background: #ff8331; margin-bottom: 5px">
          <img src="./img/logo-transparente.png" id="drawerLogo" />
        </div>
        <p class="close" @click="drawer = false">X</p>
        <h2
          v-for="link in links"
          :key="link.href"
          class="drawerlink"
          @click="[(drawer = false), $vuetify.goTo(link.href)]"
        >
          <a class="menublack">{{ link.nome }}</a>
        </h2>
      </div>
    </div>
    <div
      class="return"
      :class="{ invisible: headerFade }"
      @click="$vuetify.goTo('#inicio')"
    >
      <v-icon large> mdi-arrow-up-bold </v-icon>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      scrollY: 0,
      drawer: false,
      links: [
        { nome: "Início", href: "#inicio" },
        { nome: "Sobre", href: "#sobre" },
        { nome: "Catálogo", href: "#catalogo" },
        { nome: "Funcionários", href: "#funcionarios" },
        { nome: "Onde estamos/Contato", href: "#contato" },
      ],
    };
  },
  computed: {
    headerFade() {
      window.onscroll = () => {
        this.scrollY = window.pageYOffset;
      };
      return this.scrollY == 0 ? true : false;
    },
  },
};
</script>

<style scoped>
#links,
#hamburguer {
  margin-right: 35px;
  font-family: "Roboto Condensed", sans-serif;
  text-align: right;
  font-weight: 900;
  line-height: 70px;
  color: black;
}
div {
  display: flex;
  justify-content: space-between;
}
#logo {
  margin-top: 10px;
  margin-left: 35px;
  width: 225px;
  border-radius: 10px 10px 10px 10px;
  cursor: pointer;
}
h2 {
  padding-left: 15px;
}

.menu {
  padding: 5px;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}
.menu:hover {
  border-bottom-color: black;
}

.color {
  background-color: #ff8331;
  transition: all 0.2s;
}

.transparent {
  background-color: transparent;
  transition: all 0.2s;
}

#hamburguer {
  display: none;
}

#logoMobile {
  display: none;
}

.drawer {
  position: fixed;
  display: inline;
  top: 0;
  bottom: 0;
  left: -90%;
  width: 90%;
  background: rgb(245, 245, 245);
  box-shadow: 0px 10px 10px rgba(0, 0, 0, 0.253);
  transition: all 0.2s;
}

.show {
  left: 0px;
  transition: all 0.2s;
}

.close {
  position: absolute;
  right: 10px;
  top: 10px;
  font-size: 0.9rem;
  font-weight: 600;
  height: 20px;
  width: 20px;
  border-radius: 10px;
  display: flex;
  justify-content: center;
  background: #bbbbbb;
  user-select: none;
  cursor: pointer;
  z-index: 2;
}
.menuwhite {
  color: white;
  transition: all 0.2s;
}

.menuwhite:hover {
  border-bottom-color: white;
}

.menublack {
  color: black;
  transition: all 0.2s;
}

#drawerLogo {
  width: 350px;
  height: 100px;
}

.drawerlink {
  display: block;
  cursor: pointer;
  text-align: center;
}

.drawerlink:hover {
  background-color: rgb(185, 185, 185);
}

.return {
  transition: all 0.2s;
  opacity: 1;
  position: fixed;
  bottom: 5%;
  right: 3%;
  padding: 10px;
  background: #ff8331;
  border: none;
  outline: none;
  border-radius: 50%;
}

.invisible {
  opacity: 0;
  transition: all 0.2s;
}
@media (max-width: 970px) {
  #links {
    display: none;
  }
  #logo {
    display: none;
  }
  #hamburguer {
    display: inline;
    margin-right: 15px;
  }
  #logoMobile {
    display: inline;
    height: 70px;
    margin-left: 15px;
    cursor: pointer;
  }
}

@media (max-width: 395px) {
  #drawerLogo {
    width: 200px;
    height: 70px;
  }
}
</style>