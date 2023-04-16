<template>
  <div>
    <button @click="$emit('trocarImagem')">trocar imagem</button>
    <!-- emit= comunicação filho pro pai -->
    <!-- props= comunicação pai pro filho -->
  </div>
</template>

<script>
export default {
  name:'EmitP',
  emits:['trocarImagem']
  
};
</script>

<style></style>
