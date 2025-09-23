<script>
    export default {
        // Add Code Here
        data() {
            return {
            message: "Choose your favorite fruit:",

        // challenge: use array  
        fruits: ["apple", "orange", "peach"],
            }
        }
    }
</script>

<template>
    <div id="app">
        {{ message }} </br>
        {{ fruit1 }} <input type="radio" name="fruit">
        {{ fruit2 }} <input type="radio" name="fruit">
        {{ fruit3 }} <input type="radio" name="fruit">
        <div v-for="fruit in fruits"> 
            {{fruit}} <input type="radio" name="fruit" :value="fruit"></input>
        </div>
    </div>
</template>

<style scoped>
    div {
    margin: 10px 0;
    }
    label {
    margin-left: 5px;
    }
</style>