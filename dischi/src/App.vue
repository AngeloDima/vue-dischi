<template>
  <div>
    <headerCode />
    <mainCode />
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
  components: {
    headerCode,
    mainCode,
    footerCode,
  },
  created(){
    console.log(`Recupero dati ....`);
    axios.get(`https://flynn.boolean.careers/exercises/api/array/music`).then();

  }
}
</script>

<style lang="scss">
</style>