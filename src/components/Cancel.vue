<template>
  <button :class="{
    cancel: true
  }" :title="title" v-on:click="go('home')">✕</button>
</template>

<script>
export default {
  props: { go: Function, title: String, invert: Boolean }
}
</script>

<style scoped>
  .cancel {
    background-color: transparent;
    color: white;
    font-weight: bold;
    font-size: 2rem;
    width: 2.25rem;
    height: 2.25rem;
    cursor: pointer;
    border: 0;
    margin: 0;
    padding: 0;
    border-radius: 100%;
  }
</style>
