<template>
    <div>
        <div>
            <!--v-bind is a vue directive which links the javascript variables to the html for the inpur below, the value is coming from a js variable called title-->
            <input id="tbxItem" v-bind:value="newItem" @keyup.enter="onEnter" placeholder="Add list item"/>
            <button v-bind:value="newItem" @click="onEnter" >Add!</button>
            <!--v-on is also a vue directive, that allows to set a behavior on a specific event-->
        </div>
    </div>
</template>

<script>
    export default {
        props: ['newItem'],
        methods: {
            deleteItem(index){
              this.listItems.splice(index, 1);
            }
        },
    }
</script>

<style scoped>
</style>