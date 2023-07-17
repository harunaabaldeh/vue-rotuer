<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link :to="{ name: 'About' }">About</router-link> |
    <router-link :to="{ name: 'Jobs' }">Jobs</router-link>
  </div>

  <button @click="redirect">redirect</button>
  <button @click="back">go back</button>
  <button @click="forward">go forward</button>

  <router-view />
</template>

<script>
export default {
  data() {
    return {

    }
  },
  methods: {
    redirect() {
      this.$router.push({ name: "Home" })
    },
    back() {
      this.$router.go(-1)
    },
    forward() {
      this.$router.go(1)
    }
  }
}
</script>

<style>
button {
  margin: 0 10px;
  padding: 10px;
  border: none;
  border-radius: 4px;
  text-transform: uppercase;
  cursor: pointer;
}

#nav {
  padding: 30px;
}

#nav a.router-link-exact-active {
  color: white;
  background: crimson;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  padding: 10px;
  border-radius: 4px;
}

#app {
  text-align: center;
  color: #444;
  margin-top: 60px;
}

body {
  margin: 0;
  background: #eee;
}
</style>
