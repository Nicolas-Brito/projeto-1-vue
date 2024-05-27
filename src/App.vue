<template>
<div>
  <ul>
   <li v-for="(item,index) in items" :key="index" v-bind:class="{'item-selected':index===itemselecionado}" @mouseover="seleciona(index)" @mouseleave="voltar">

   {{ item }}  
  </li>
  </ul>
</div>
</template>

<script>
export default{
  data(){
    return{
    items: ["pao com ovo","hamburguer","pizza","pastel","sushi"],
    itemselecionado:-1
    };
  },
  methods:{
    seleciona(index){
      this.itemselecionado=index
    },
    voltar(){
      this.itemselecionado=-1
    }
  }
}
</script>


<style>
.item-selected{
  background-color: red;
}
</style>

