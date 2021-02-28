<template>
  <input type="checkbox" :checked="checked" @change="updateCheckbox" />
</template>

<script>
export default {
  name: "MyCheckbox",
  props: {
    checked: Boolean,
  },
  model: {
    prop: "checked",
    event: "change",
  },
  methods: {
    updateCheckbox(e) {
      this.$emit("change", e.target.checked);
    },
  },
};
</script>

<style>
</style>
