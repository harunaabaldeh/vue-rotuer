<template>
    <h2>404</h2>
    <h3>Page not found</h3>
    <div class="home">
        <router-link :to="{ name: 'Home' }"> 👉Go back to home</router-link>
    </div>
</template>
<script>
export default {

}
</script>
<style>
.home a {
    text-decoration: none;
    cursor: pointer;
    color: white;
    background: crimson;
    padding: 12px;
    border-radius: 6px
}
</style>