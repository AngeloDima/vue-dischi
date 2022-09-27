<template>
    <div class="Midle">
        <div v-for="characters in characters" :key="characters.id"></div>
    </div>
</template>

<script>
    export default {
  name: 'mainCode',
  props: {
    characters: Array
  }
}
</script>

<style lang="scss" scoped>
    .Midle{
        width: 100%;
        height: 80vh;
        background-color: #00ff84;
    }
    </style>