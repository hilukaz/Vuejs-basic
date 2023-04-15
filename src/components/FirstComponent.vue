<template><!--indica onde o html vai ficar-->
    <div><!--os componentes do view só pode ter um elemento base, por isso envolve todo o html dentro de uma div-->
        <h1>Olá vue</h1>
        <p>esse {{texto}} um {{props}} </p>
    </div>
</template>

<script>
    export default{
        name:'FirstComponent',  
        data(){
            return{
                texto:'é',
                texto2:'objeto'
            }
        },
        props:{
            props: String
        }
    }
</script>
