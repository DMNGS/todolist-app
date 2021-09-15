<!--
Author : DOMINGUES PEDROSA Samuel
-->
<template>
<div>
    <li>
        <item v-for="item in listItems" :key="item" :itemName="item"></item>
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
    }
}
</script>

<style>
</style>