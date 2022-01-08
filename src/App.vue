<template>
  <div id="nav">
    <router-link to="/about">Take A turn</router-link> |
    <router-link to="/">Home</router-link> |
    <div class="acount">
      <router-link to="/about">Log in</router-link> /
      <router-link to="/about">Register</router-link>
    </div>
  </div>
  <router-view/>
  <footer>
    <span>Inicio</span>
    <span>Log In</span>
    <span>Register</span>
    <span>Take a turn</span>
  </footer>
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Mukta&display=swap');
body{
    background: #ffc;
}
#app {
  font-family:  'Mukta', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  font-size: 3vh;
}

#nav {
  padding: 30px;
  text-align: center;
  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #f91;
    }
  }
  .acount{
    display: inline;
  }
}
</style>
