<template>
  <div>
    <headerCode />
    <mainCode :character="characters"/>
    <footerCode />
  </div>
</template>

<script>
import axios from "axios";

import headerCode from './components/headerCode.vue';
import mainCode from './components/mainCode.vue';
import footerCode from './components/footerCode.vue';



export default {
  name: 'App',
  data(){
    return {
      characters: []
    }
  },

  components: {
    headerCode,
    mainCode,
    footerCode,
  },

  created(){
    console.log(`Recupero dati ....`);
    axios.get(`https://flynn.boolean.careers/exercises/api/array/music`)
    .then(({status, datiCard})=>{
      if(status === 200){
        this.characters = datiCard;
        console.log(this.characters);
      }
    });

  }
}
</script>

<style lang="scss">
</style>