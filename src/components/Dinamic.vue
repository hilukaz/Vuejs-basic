<template>
    <img v-bind:src="avatar" alt="">
    <!--v-bind:src ou href//// : simplificado-->
    <!--atributo dinâmico, ele pode ser um link href, ou imagem-->
    <Emit @trocarImagem="mudarImagem"/>
    <!-- a emissão do evento trocar imagem ativou o mudar imagem -->
</template>

<script>
import Emit from "./emit.vue";
    export default{
        name:'DinamicP',
        data(){
            return{
                avatar:'/favicon.ico',
                boolean:1
            }
        },
        components:{
            Emit
        },
        methods:{
            mudarImagem(){
                if (this.boolean===1) {
                    this.avatar='/favicn.ico'
                    this.boolean=0
                }else{
                    this.avatar='/favicon.ico'
                    this.boolean=1
                }
            }
        }
    }
</script>
<style scoped>
    img{
        max-width: 30px;
    }
</style>