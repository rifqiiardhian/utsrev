// ---------------------------------------
// Copyright 2020
// Created and Designed by Rifqi Ardhian
// Authentic Design
// User Interface Mid Test
// ---------------------------------------

<template>
  <div id="app">
    <link rel="stylesheet"
            href="https://use.fontawesome.com/releases/v5.2.0/css/all.css"
            integrity="sha384-hWVjflwFxL6sNzntih27bfxkr27PmbbK/iSvJ+a4+0owXq79v+lsFkW54bOGbiDQ"
            crossorigin="anonymous">
        <div>
            <b-navbar class="navbar" id="nav" toggleable="lg" fixed="top">
                <b-navbar-brand  class="navbar-brand m-auto" href="#home">
                    <img src="./assets/images/logojam.png" alt="logo" class="logo">
                </b-navbar-brand>
                <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
                <b-collapse id="nav-collapse" class="nav-collapse" is-nav>
                    <b-navbar-nav class="mr-auto">
                        <b-nav-item class="nav-item" href="" right>Home</b-nav-item>
                        <b-nav-item class="nav-item" href="" right>About Us</b-nav-item>
                        <b-nav-item class="nav-item" href="" right>Men Watch</b-nav-item>
                        <b-nav-item class="nav-item" href="" right>Women Watch
                        </b-nav-item>
                    </b-navbar-nav>
                </b-collapse>
                <b-collapse id="nav-collapse" class="nav-collapse" is-nav>
                    <b-navbar-nav class="ml-auto">
                        <b-nav-item class="nav-item" href="" right>
                            <i class="fas fa-search"></i>
                        </b-nav-item>
                        <b-nav-item class="nav-item" href="" right>
                            <i class="fas fa-user"></i>
                        </b-nav-item>
                        <b-nav-item class="nav-item" href="" right>
                            <i class="fas fa-shopping-cart"></i>
                        </b-nav-item>
                    </b-navbar-nav>
                </b-collapse>
            </b-navbar>
        </div>
        <indexpage/>
  </div>
</template>

<script>
import indexpage from './views/index.vue';

export default {
  name: 'App',
  components: {
    indexpage,
  },
  mounted() {
    this.$nextTick(() => {
      window.addEventListener('scroll', () => {
        const navbar = document.getElementById('nav');
        // eslint-disable-next-line camelcase
        const nav_class = navbar.classList;
        if (document.documentElement.scrollTop >= 150) {
          if (nav_class.contains('shrink') === false) {
            nav_class.toggle('shrink');
          }
        } else if (nav_class.contains('shrink') === true) {
          nav_class.toggle('shrink');
        }
      });
    });
  },
};
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
@import 'css/app.css';
@import 'css/style.css';
</style>
