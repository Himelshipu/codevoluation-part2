<template>
  <div>

    <h3>This is a Pop Up</h3>
    <input type="text" placeholder="inset Your Name" name="name" v-model="name">
    <input type="text" placeholder="inset Your Father's Name" name="fName" v-model="fName">
    <button @click="$emit('cancel',fName,name)"> Close</button>

  </div>
</template>

<script>
export default {
  name:'PopUp',
  // emits:['cancel'],
  emits:{
    cancel: (fName)=>{
      if(!fName){
        return false
      }else {
        return true
      }
    }
  },
  data(){
    return{
      name:'',
      fName:''

    }
  },
}
</script>

<style scoped>

</style>