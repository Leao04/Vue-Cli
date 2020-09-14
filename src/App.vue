<template>
  <div id="app">
    <Header @click="goTo('index')" />

    <nav>
      <a class="esquerda" href="/" @click.prevent="goTo('index')">Principal</a>
      <a class="direita" href="/sobre" @click.prevent="goTo('about')">Sobre</a>
    </nav>
    <main>
      <transition name="fade" mode="out-in">
        <index v-if="currentPage === 'index'" />
        <about v-else-if="currentPage === 'about'" />
        <p v-else>Página não encontrada.</p>
      </transition>
    </main>

    <footer class="final">
      <Footer />
    </footer>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import index from "./pages/index";
import about from "./pages/about";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    index,
    about,
    Footer,
  },
  data() {
    return {
      currentPage: "index",
    };
  },
  methods: {
    goTo(page) {
      this.currentPage = page;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.esquerda {
  padding-right: 20px;
}

.final {
  position: absolute;
  bottom: 0px;
  width: 99%;
}
</style>
