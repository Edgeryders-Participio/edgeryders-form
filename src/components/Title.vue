<template>
  <div>
    <img v-if="image" :src="image" alt="Aalto University on 31st of March 2020">
    <h1 class="title" v-if="!image && title">{{displayTitle}}</h1>
    <h3 class="subtitle" v-if="!image && subtitle">{{subtitle}}</h3>
    <p class="instructions" v-html="instructions" v-if="instructions">{{instructions}}</p>
    <p class="consent" v-html="consent" v-if="consent">{{consent}}</p>
  </div>
</template>

<script>
export default {
  props: {
    index: Number,
    title: String,
    subtitle: String,
    instructions: String,
    consent: String,
    image: String,
  },
  computed: {
    displayTitle() { return this.title.replace(/{{index}}/, this.index) }
  }
}
</script>

<style scoped>
  .title {
    font-family: 'Libre Baskerville', serif;
    margin-top: 0;
    max-width: 25rem;
  }

  .subtitle {
    font-family: 'Libre Baskerville', serif;
    margin-top: 0;
    max-width: 25rem;
  }

  .instructions {
    font-family: 'Source Sans Pro', sans-serif;
    max-width: 25rem;
  }

  .consent {
    font-family: 'Source Sans Pro', sans-serif;
    max-width: 25rem;
    font-size: 0.8rem;
  }
</style>
