<template>
  <div>
    <ul>
      <!-- <li v-for="(tech,index) in tecnologia" v-bind:key="index">{{tech}}</li> -->
      <li v-for="tech in tecnologiaobject" v-bind:key="tech.id">
          {{tech.language}}
      </li>
      <!--condição no elemento selecionado-->
      <!-- key=id -->
    </ul>
  </div>
</template>
<script>

export default {
  name: 'TecnologiaInfo'
  ,data(){
    return{
      // tecnologia:['Javascript','PHP','Python']
      tecnologiaobject:[
        {id: 1, language:'Javascript'},
        {id: 2, language:'PHP'},
        {id: 3, language:'Python'},
      ]
    }
  }
}
</script>

<style scoped>
 div{/**claro os elementos não pode se contrapor */
 /** enfim se vc tirar o scope, toda a aplicação mudará de cor */
  color: red;
 }
</style>