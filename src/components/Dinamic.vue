<template>
    <img v-bind:src="avatar" alt="">
    <!--v-bind:src ou href//// : simplificado-->
    <!--atributo dinâmico, ele pode ser um link href, ou imagem-->
</template>

<script>
    export default{
        name:'DinamicP',
        data(){
            return{
                avatar:'/favicon.ico'
            }
        }
    }
</script>
