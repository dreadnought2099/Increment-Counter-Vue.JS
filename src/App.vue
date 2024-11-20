<template>
  <div class="main-container">
    <h1>Parent Component</h1>
    <h2>Counter Component</h2>
    <div>
      <p>Current count: {{ latestCount }}</p>
      <Counter @update-count="handleUpdatedCount" />
    </div>
  </div>
</template>

<script>
import Counter from "./components/Counter.vue";
import "./styles/Counter.css";

export default {
  name: "App",
  components: {
    Counter,
  },
  data() {
    return {
      latestCount: 0,
    };
  },
  methods: {
    handleUpdatedCount(count) {
      this.latestCount = count;
    },
  },
};
</script>
