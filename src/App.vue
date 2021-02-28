<template>
  <div id="app">
    <MyInput v-model="val"></MyInput>
    <br />
    <MyCheckbox v-model="checked"></MyCheckbox>
    <h1>my input: {{ val }}</h1>
    <h1>my checkbox: {{ checked }}</h1>
  </div>
</template>

<script>
import MyInput from "@/components/MyInput.vue";
import MyCheckbox from "@/components/MyCheckbox.vue";

export default {
  name: "App",
  components: {
    MyInput,
    MyCheckbox,
  },
  data() {
    return {
      val: "",
      checked: false,
    };
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
