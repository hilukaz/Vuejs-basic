<template>
  <div >
    <p v-if="condicao">Estou trabalhando no momento.</p><!--se condicao == true exiba a tag-->
    <!--todo if é preciso de um else em seguida-->
    <p v-else >Não estou trabalhando</p><!--um em baixo do outro-->
    <p class="global">Utilizo as seguintes tecnologias:</p>
    <TecnologiaInfo/>
    <p v-show="condicao">email:{{email}}</p><!--condição sem precisar de else-->
    <div >
      <button @click="showEmail">{{buttontxt}}</button><!--ao clicar ative o method showEmail-->
    </div>
    <Dinamic/>
  </div>
</template>
<script>
import TecnologiaInfo from "./Info/Tecnologia.vue";
import Dinamic from "./Dinamic.vue";

export default {
    name: 'InfoA',//O vuejs só considera componente quando estiver em formato camelCase
    components:{//hierarquia de componentes
    //a componentização serve para declarar arquivos reutilizaveis
        TecnologiaInfo,
        Dinamic,
    },
    data(){
      return{
        condicao:true,
        email:'a@gmail',
        buttontxt:'ocultar email'
      }
    },
    methods:{
      showEmail(){
        this.condicao=!this.condicao//true="true->"
        //false = !false->true
        if(!this.condicao){
          this.buttontxt='mostrar email'
        }else{
          this.buttontxt='ocultar email'
        }
      }
    }
}
</script>