<template>
    <div class="">
        <h1>usando...: {{nome}}</h1>
    </div>
</template>

<script>
export default{
    name:'LyfeC',
    data(){//atribui um valor a uma variável dentro do código
        return{
            nome:'ainda não sei'
        }
    },
    created(){//executa o método dps que o componente é criado
        setTimeout(() => {//executa o método depois de 1000 milissegundos
            this.nome="created"
        }, 1000);
    },
    mounted(){//é acionado após a renderização inicial do componente, quando o componente já está no DOM.
        setTimeout(() => {
            this.nome='mounted'
        }, 2000);
    }
}
</script>
