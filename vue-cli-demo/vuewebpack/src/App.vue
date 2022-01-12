<template>
  <div id="app">
    <!-- <HelloWorld/> -->
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">Navbar</a>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <router-link class="nav-link" to="/index">Home</router-link>
            </li>
            <li class="nav-item">
              <!-- <router-link class="nav-link" :to="{name: '首頁'}">Home</router-link> -->
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/page">Page</router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <img src="./assets/logo.png" alt="..." />
    <router-view name="menu"></router-view>
    <div class="container">
      <router-view></router-view>
    </div>  

  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
  created() {
    this.$http.get("https://randomuser.me/api/").then((response) => {
      console.log(response.data);
    });
  },
};
</script>


