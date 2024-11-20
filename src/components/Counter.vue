<template>
  <div>
    <div>
      <button class="button1" @click="decrement">Decrement</button>
      <button class="button2" @click="increment">Increment</button>
    </div>
    <div>
      <p>Current count in parent:</p>
      <p class="count">{{ count }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Counter",
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    increment() {
      this.count++;
      this.$emit("update-count", this.count);
    },
    decrement() {
      this.count--;
      this.$emit("update-count", this.count);
    },
  },
};
</script>
