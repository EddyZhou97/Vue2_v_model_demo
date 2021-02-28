<template>
  <input type="checkbox" :checked="checked" @change="updateCheckbox" />
</template>

<script>
export default {
  name: "MyCheckbox",
  props: {
    checked: Boolean,
  },
  // 通过定义model中的 prop 和 event 来重载默认的 value 属性和 input 事件
  model: {
    // 绑定的属性
    prop: "checked",
    // 触发的事件
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
