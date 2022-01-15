<template>
  <div id="app">
    <img class="img" alt="Vue logo" src="./assets/logo.png">
    <h2 class="pt-2"> Contador</h2>

    <div class="row">
      <div class="col-12 text-center">
        <h1 class="pb-2"><strong>{{ number }}</strong></h1>
          <div>
            <button @click="addCount" class="mr-2 btn btn-success btn-sm">Adicionar</button>
            <button @click="removeCount" :disabled="number === 0" class="btn btn-danger btn-sm">Remover</button>
          </div>
      </div>
    </div>
    <div class="row pt-5">
      <div class="col-12 text-center">
        <span><i class='bx bxl-github mr-2'></i></span><small>@CarolinaBrilhante </small>
      </div>
    </div>
  </div>
</template>

<script src="https://cdn.jsdelivr.net/npm/jquery@3.5.1/dist/jquery.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.6.1/dist/js/bootstrap.bundle.min.js" integrity="sha384-fQybjgWLrvvRgtW6bFlB7jaZrFsaBXjsOMm/tB9LTS58ONXgqbR9W8oWht/amnpF" crossorigin="anonymous"></script>

<script>

export default {
  name: 'App',
  components: {
  },
  data(){
    return {
      number: 0

    }
  },
  methods: {
    addCount(){
      this.number++
      console.log('Adicionado')
    },
    removeCount(){
      if(this.number > 0){
        this.number--
        console.log('Removido')
      }
    },
  }
}
</script>

<style>
@import "https://cdn.jsdelivr.net/npm/bootstrap@4.6.1/dist/css/bootstrap.min.css";
@import "https://unpkg.com/boxicons@2.1.1/css/boxicons.min.css";

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.img {
  width: 120px;
  height: 120px;
}
</style>
