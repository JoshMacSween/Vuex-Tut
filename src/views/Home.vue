<template>
  <div class="home">
    <h3>{{ joke }}</h3>
    <button @click="addJoke">Add Joke</button>
  </div>
</template>

<script>
// @ is an alias to /src
import {mapActions} from 'vuex'

export default {
  name: "Home",
  data: () => ({
    // joke: "",
  }),
  methods: {
    ...mapActions(["setCurrentJoke"]),
    addJoke() {
      // this.$store.dispatch("setCurrentJoke");
      this.setCurrentJoke()
    },
  },
  computed: {
    joke() {
      return this.$store.getters.getCurrentJoke;
    },
  },
  // mounted() {
  //   this.joke = this.$store.getters.getCurrentJoke;
  // },
};
</script>
