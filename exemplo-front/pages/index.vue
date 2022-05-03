<template>
  <div class="container">
    <h1> Lista de pessoas e idades </h1>
    <ul>
      <li :key="item.id" v-for=" item in pessoas ">
        {{item.nome}} - {{item.idade}} anos
      </li>
    </ul>
    <button @click="digaOla">Diga Olá!</button>
  </div>
</template>

<script>
export default {
  data: function(){
    return {
      titulo : "Lista de pessoas e idades",
      pessoas: [
        {id: 1, nome:"Annabeth Chase", idade: "18"},
        {id: 2, nome:"Percy Jackson", idade: "19"},
        {id: 3, nome:"Jung Jungkook", idade: "23"},
        {id: 4, nome:"Kim Taehyung", idade: "24"},
      ]
    }
  },
  methods:{
    digaOla: function(){
      alert("Olá Mundo do Nuxt.js!")
    }
  }
}
</script>

<style scoped>
.container{
  margin: 20px;
}
</style>
