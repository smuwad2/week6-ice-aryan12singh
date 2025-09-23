<script>
    export default { 
        data() {
            return {
                selectedOption: 'username',
                username: '',
                email: ''
            }
        }
    }
</script>

<template>
    <h1>Please select your login option</h1>
    <!-- Add/modify code in the following to have a dropdown list 
        which lets the user to select either to login with username or email -->
    <select v-model="selectedOption">
        <option value="username">Username login</option>
        <option value="email">Email login</option>
    </select>

    <div v-if="selectedOption === 'username'">
        <label>Username</label>
        <input name="username" v-model="username" placeholder="Enter your username">
    </div>
    
    <div v-else>
        <label>Email</label>
        <input type="email" name="email" v-model="email" placeholder="Enter your email">
    </div>
</template>

