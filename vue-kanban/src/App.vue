<template>
  <div id="nav">
    <router-link to="/"><i class='xi-home-o'></i></router-link>
    <router-link to="/my_info" v-if="$isLogin()"><i class='xi-user-o'></i></router-link>
    <router-link to="/join" v-else><i class="xi-user-plus-o"></i></router-link>
    <router-link to="/logout" v-if="$isLogin()"><i class="xi-log-out"></i></router-link>
    <router-link to="/login" v-else><i class='xi-log-in'></i></router-link>
    <router-link to="/kanban" v-if="$isLogin()">
      <i class='xi-view-module'></i>
    </router-link>
  </div>
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}
#nav a {
  font-weight: bold;
  color: #2c3e50;
}
#nav a.router-link-exact-active {
  color: #42b983;
}
</style>