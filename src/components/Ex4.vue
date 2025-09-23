<script>
    export default { 
        data() {
            return {
                isRed: false,
                id: 'demo1'
            }
        },
        methods: { 
            toggleColor() {
                this.isRed = !this.isRed;
            }
        }
    }
</script>

<template>
    <!-- Modify code here -->
    <div class="container">
        <div v-bind:id="id" v-bind:class="isRed ? 'redBox m-2' : 'blueBox m-2'">
            div ID : {{id}} 
        </div>
        
        <button type="button" v-bind:class="isRed ? 'btn btn-danger' : 'btn btn-primary'" v-on:click="toggleColor">Change Color</button>
    </div>
</template>

<style scoped>
    .redBox {
        background-color: red;
    }
    .blueBox {
        background-color: blue;
    }
    #demo1 {
        color: white;
    }
</style>
