<template>
  <div> 
    <div class="card">
      <nav aria-label="breadcrumb">
        <ol class="breadcrumb mb-0">
            <li class="breadcrumb-item"><a href="#">{{itemSelecionado.type}}</a></li>
            <li class="breadcrumb-item active" aria-current="page">{{itemSelecionado.name}}</li>
        </ol>
      </nav>     
    
      <div class="card-body">
        <img v-bind:src="itemSelecionado.image" class="card-img-top mt-0 mb-2">        
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'PokeImg',
  props: {
    item: Object
  },
  data() {
    return {
      itemSelecionado: Object
    }
  },
  watch: { 
    item(e) {
      this.itemSelecionado = e;
    }
  }  
}
</script>


<style scoped>

</style>