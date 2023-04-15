<template>
  <div>
    <FirstComponent v-bind:props="props"/>
    <!-- v-bind para transmitir uma variável pela tag, sem o vbind vc estará transmitindo uma string -->
    <!-- entender dados -->
    <LifeCycleHook/>
    <InfoA/>
    <Forms/>
  </div>
</template>

<script>
  import FirstComponent from "./components/FirstComponent.vue";//importar o objeto em si
  import LifeCycleHook from "./components/LifeCycleHook.vue";
  import InfoA from "./components/Info.vue";
  import Forms from './components/Form.vue'

  export default{
    name:'App',
    components:{//quais componenstes estarão na página
      FirstComponent,
      LifeCycleHook,
      InfoA,
      Forms
    },
    data(){
      return{
        props:'objeto do props'
        // capacidade de transmitir uma variável pai para uma filho
      }
    }
  }
</script>

<style >/* global, altera todas as páginas independente da classe hierarquica*/
  div {
    background-color: #333;
    color: #FFF;
  }
</style>