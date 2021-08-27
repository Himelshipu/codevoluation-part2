<template>
<h3>Component C Contents</h3>
  <ComponentE />
</template>

<script>
import ComponentE from './ComponentE.vue'
export default {
  name: 'ComponentC',
  components: {
   ComponentE
  },
  data(){
    return{

    }
  }
}

</script>

<style>

</style>