<template>
  <div id="app">
    <button @click="increment">+</button>
    {{ $store.state.count }}
  </div>
</template>

<script>
import { mapActions } from "vuex";
import store from "./store/survey";

export default {
  store,
  name: "App",
  components: {},
  computed: {
    count: () => this.$store.state.count,
  },
  methods: mapActions(["increment"]),
};
</script>
