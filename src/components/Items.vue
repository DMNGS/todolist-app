<!--
Author : DOMINGUES PEDROSA Samuel
-->
<template>
<div>
    <li>
        <item v-for="(item, index) in listItems" :key="item" :itemName="item" :index="index"></item>
    </li>
</div>
</template>

<script>
import Item from "./Item.vue"

export default {
    name : "items",
    props: ["listItems"],
    components: {
        Item,
    },
    data() {
        return{
            itemName: "AHHHHHHHHH"
        }
    },
    methods: {
        onEnter (event) {
            this.$emit('onEnter', event.target.value);
            //this.title = "";
        }
    },
}
</script>

<style>
</style>