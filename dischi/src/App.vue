<template>
  <div>
    <headerCode />
    <mainCode />
    <footerCode />
  </div>
</template>

<script>
import headerCode from './components/headerCode.vue'
import mainCode from './components/mainCode.vue'
import footerCode from './components/footerCode.vue'

export default {
  name: 'App',
  components: {
    headerCode,
    mainCode,
    footerCode,
    
  }
}
</script>

<style lang="scss">

</style>
