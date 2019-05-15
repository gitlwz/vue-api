<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">具名插槽</router-link> |
      <router-link to="/about">作用域插槽</router-link>
      <router-link to="/is">is</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style>
header{
    height: 50px;
}
main{
    min-height: 50px;
}
footer{
    height: 50px;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
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
.title{
    background-color: #678;
}
</style>
