<template>
  <h3 >Component E Contents = {{castName}}</h3>
  <ComponentF />
</template>

<script>
import ComponentF from './ComponentF.vue'
export default {
  name: 'ComponentE',
  inject:['castName'],
  components: {
    ComponentF
  },
  data(){
    return{

    }
  }
}

</script>

<style>

</style>