<template>
  <div>
    <nav class="navbar navbar-expand-sm navbar-light" bg-gradient-danger text-white style="background-color:#FE4D55">
      <img id="logo" src=".\assets\Restaurant Tinder Logo.png" width="50vh">
      <a class="navbar-brand" style="font-family:'Grape Nuts', cursive;" href="../"><strong>Restaurant Tinder</strong> </a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation"><span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item active">
          <a class="nav-link" href="#"><router-link class="nav-link" v-bind:to="{ name: 'home' }"><h5>Home</h5></router-link></a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#"><router-link class="nav-link" v-bind:to="{ name: 'logout' }" v-if="$store.state.token != ''"><h5>Logout</h5></router-link></a>
          </li>
        </ul>
      </div>
    </nav>
    <br>
    <router-view />
  </div>
</template>
<style>
@import url('https://fonts.googleapis.com/css2?family=Grape+Nuts&display=swap');
.navbar-brand{
  font-size: 2em;
  color: white;
  background-color: #FE4D55;
  margin-top: -8px;
  margin-bottom: -8px;
  margin-left: 5px;
}
.navbar-toggler{
  font-size: 1em;
  background-color: none;
  margin-right: 10px;
}
.collapse{
  margin-top: 7px;
  margin-left: 10px;
}
#logo{
  margin-left: 10px;
}
</style>