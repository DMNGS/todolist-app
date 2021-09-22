<!--
Author : DOMINGUES PEDROSA Samuel
-->
<template>
  <div>
    <input type="checkbox" />
    <label>{{ itemName }}</label>
    <button @click="onClick" v-bind:value="index"><i class="fas fa-trash"></i></button>
  </div>
</template>

<script>
export default {
  name: "item",
  props: ["itemName", "index"],
  methods: {
    onEnter(event) {
      this.$emit("onClick", event.target.value);
      //this.title = "";
    },
  },
};
</script>

<style>
</style>