<template>
  <nav>
    <router-link to="/">Home</router-link>
    <router-link to="/about">About</router-link>
    <router-link to="/jobs">Jobs</router-link>
  </nav>
  <button @click="go">Go</button>
  <button @click="back">Back</button>
  <button @click="redirect">Redirect</button>
  <router-view/>
</template>
<script>
export default{
  methods:{
go(){
  this.$router.go(1)
},
back(){
  this.$router.go(-1)
},
redirect(){
  this.$router.push({name:"Jobs"})
}
  }
}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  padding: 10px;
  border-radius: 4px;
}

nav a.router-link-exact-active {
  color: #e6ece9;
  background: crimson;
 
}
</style>
