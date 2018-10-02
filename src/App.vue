<template>

  <div id="app" class="container-fluid">
     <div class="logo-container">
       <img src="./assets/LOGO1.png" class="logo">
     </div>
    

    <todo-list></todo-list>

  </div>

</template>

<script>

import TodoList from './components/TodoList'


export default {
  name: 'App',
  components: {  
    TodoList
  }
}
</script>

<style>

body {
  background: #333;
}

* {
  box-sizing: border-box;
}
.container-fluid {
margin: 0 auto;
width: 100%;
height: 100vh;
background-image: url(https://source.unsplash.com/category/wallpaper/1920x1080);
background-repeat: no-repeat;
background-size: cover;
background-position: center center;
}


#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
  padding-top: 40px;
  font-size: 24px;
 
}

.logo-container {
  background: rgba(255,255,255,0.5);
  padding: 10px;
  clip-path: polygon(55% 0, 100% 0, 100% 100%, 0 100%, 18% 5%);
  max-width: 600px;
  margin: 0 auto;
}

.logo {
  display: block;
  margin: 10px auto;
 
  height: 75px;
}
</style>
