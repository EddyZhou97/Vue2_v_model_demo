<template>
  <input type="text" :value="value" @input="updateInput" />
</template>

<script>
export default {
  name: "MyInput",
  props: {
    value: String,
  },
  methods: {
    updateInput(e) {
      this.$emit("input", e.target.value);
    },
  },
};
</script>

<style>
</style>
