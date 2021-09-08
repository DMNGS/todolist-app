<template>
    <div>
        <div>
            <em>Set a title and press Enter</em> <!--This is the text that appears above the input -->
            <!--v-bind is a vue directive which links the javascript variables to the html for the inpur below, the value is coming from a js variable called title-->
            <input v-bind:value="title" @keyup.enter="onEnter"/>
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
        }
    }
</script>

<style scoped>
</style>