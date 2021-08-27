<template>
  Hello {{username}}!!  Are You {{ heroname }}?
  <br>
</template>
<script>
export default {
  name: 'Greet',
  props:['username','heroname']
}

</script>
<style>

</style>