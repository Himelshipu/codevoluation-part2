<template>
  <button @click="showPopUp = true"> SHOW POPUP</button>
  <br>
  <PopUp v-show="showPopUp" @cancel = "closePopUp" />

  Main --- {{cast}}

  <ComponentC/>
  <hr>
  <Greet />
  <Greet username="Maksudur" heroname="superman"/>
  <Greet username="Rahman" heroname="batman"/>
  <Greet username="shipu" heroname="spiderman"/>
  <Greet v-bind:username="nickname" v-bind:heroname="designation"/>
 <Greet />
  <hr>
  <Article title="Loream Lipsum" v-bind:likes="98" :isPublished="true" id="my-article"/>

</template>

<script>
import Greet from './components/Greet.vue'
import Article from './components/Article.vue'
import ComponentC from './components/ComponentC.vue'
import PopUp from './components/PopUp.vue'

export default {
  name: 'App',
  components: {
    Greet,Article,ComponentC,PopUp
  },

  data(){
    return{
      nickname:'himel',
      designation:'web developer',
      cast:"sunni",
      showPopUp:false,
    }
  },

  methods:{
    closePopUp(fName ,name){
      this.showPopUp = false
      console.log('hello',fName ,name)
    }
  },


  provide (){
    return{
      castName: this.cast,
    }

  },

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #fff;
  margin: 60px;
  padding: 30px;
  background:#2c3e50 ;
}
</style>
