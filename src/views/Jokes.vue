<template>
  <div class="jokes">
    <h1>All Jokes Here</h1>
    <h4 v-for="(joke, idx) in jokes" :key="idx">
      <span>{{ idx + 1 }}</span>
      {{ joke }}
    </h4>
  </div>
</template>

<script>
export default {
  computed: {
    jokes() {
      return this.$store.getters.getAllJokes;
    },
  },
};
</script>
