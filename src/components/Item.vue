<!--
Author : DOMINGUES PEDROSA Samuel
-->
<template>
<div>
    <input type="checkbox">
    <label>{{itemName}}</label>
</div>
</template>

<script>
export default {
    name: "item",
    props: ['itemName']
}
</script>

<style>
</style>