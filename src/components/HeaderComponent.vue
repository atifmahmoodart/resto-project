<template>
    <div class="nav">
        <router-link to="/">Home</router-link>
        <router-link to="add">Add Restaurant</router-link>
        <router-link v-on:click="logout" to="login">Logout</router-link>


    </div>
</template>

<script>
export default {
    name: 'HeaderComponent',
    methods: {
        logout() {
            localStorage.clear();
            this.$router.push({ name: 'Login' })
        }
    }
}
</script>

<style>
.nav {
    background-color: #333;
    overflow: hidden;
}

.nav a {
    float: left;
    color: #f2f2f2;
    text-align: center;
    padding: 16px 14px;
    text-decoration: none;
    font-size: 16px;
    margin-right: 4px;
}

.nav a:hover {
    background-color: #9f2929;
    color: #901313;
}
</style>