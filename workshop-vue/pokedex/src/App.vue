<template>
  <div id="app" class="conteiner">
    <div class="col-12 row">
      <aside class="col-5">
        <PokeLista @pokemon-selecionado="alteraPokemon"></PokeLista>
      </aside>
      <div class="col-7">
        <PokeImg :item="pokemonSelecionado"></PokeImg>
      </div>
    </div>
  </div>
</template>

<script>
import PokeLista  from './components/PokeLista.vue'
import PokeStats  from './components/PokeStats.vue'
import PokeImg  from './components/PokeImg.vue'

export default {
  name: 'app',
  components: {
    PokeLista,
    PokeImg,
    PokeStats
  },
  data() {
    return {
      pokemonSelecionado: undefined
    }
  },
  methods: {
    alteraPokemon(e) {
      this.pokemonSelecionado = e;
    }
  }
};
</script>

<style>
@import '../node_modules/bootstrap/dist/css/bootstrap.css';
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
