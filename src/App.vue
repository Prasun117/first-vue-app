<template>
  <div id="app">
    <nav>
      <router-link to="/"> Home </router-link> |
      <router-link to="/about"> About </router-link>|
      <router-link to="/weather"> weather app</router-link>|
       <router-link to="/poc"> Poc app</router-link>
    </nav>
    <router-view />
  </div>
</template>

<script>
export default {};
</script>

<style>
html {
  box-sizing: border-box;
}
*,
*:before,
*:after {
  box-sizing: inherit;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
