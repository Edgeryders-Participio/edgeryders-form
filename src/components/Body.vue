<template>
  <p class="body" v-if="body" v-html="body" />
</template>

<script>
export default {
  props: { body: String },
}
</script>

<style scoped>
  .body {
    max-width: 80%;
    font-family: 'Source Sans Pro', sans-serif;
    font-size: 1.1rem;
    margin: 0 0 4rem 0;
  }
</style>
