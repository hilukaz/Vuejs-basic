<template>
    <div >
  <form>
    <label for="name">Nome:</label>
    <input type="text" id="name" v-model="name">
    <!-- v-model= value -->
    
    <label for="email">E-mail:</label>
    <input type="email" id="email" v-model="email">
    
    <button type="submit" v-on:click.prevent="submitForm">Enviar</button>
    <!-- prevent. não permite atualizar a página -->
  </form>
    </div>
</template>

<script>
    export default{
        name:'FormS',
        data(){
            return{ 
                name: '',
                email:'',
            }
        },
        methods: {
            submitForm() {
                console.log('Formulário enviado!');
                console.log('Nome: ' + this.name);
                console.log('E-mail: ' + this.email);
            }
        }   
    }
</script>
