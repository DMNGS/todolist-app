<template>
    <div>
        <div>
            <!--v-bind is a vue directive which links the javascript variables to the html for the inpur below, the value is coming from a js variable called title-->
            <input v-bind:value="title" @keyup.enter="onEnter" placeholder="Add list item"/>
            <button v-bind:value="title" @click="onEnter" >Add!</button>
            <!--v-on is also a vue directive, that allows to set a behavior on a specific event-->
        </div>
    </div>
</template>

<script>
    export default {
        props: ['title'],
        methods: {
            onEnter (event) {
                this.$emit('onEnter', event.target.value);
                //this.title = "";
            }
        },
    data() {
        return {
        title: 'My VueJS Todo List',
        listItems: ["Miiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiilk", "Tattoed chicken", "Whale greace", "lemons"]
    };
  },
    }
</script>

<style scoped>
</style>