<template>
  <v-app>
    <Header class="scroll2"/>


    <v-btn
      fab
      class="btnn"
      @click="nextRouting"
      :to="routes[index]"
    >
      <v-icon>mdi-play</v-icon>
    </v-btn>


    <div class="routing">
      <v-app-bar-nav-icon
        @click="drawer = !drawer"
        style="
        position: fixed;
        top: 20px;
        right: 20px;
        z-index: 2000;
        font-size: 40px!important;
"
        class="navIcon"
      ></v-app-bar-nav-icon>

      <v-navigation-drawer
        v-model="drawer"
        class="main-div"
        width="500px"
        fixed
        right
        app
      >
        <nav class="wrapper">
          <ul class="padding-top">
            <li>
              <NuxtLink class="NuxtLink" to="/home">Home</NuxtLink>
            </li>
            <li>
              <NuxtLink class="NuxtLink" to="/about">About</NuxtLink>
            </li>
            <li>
              <NuxtLink class="NuxtLink" to="/services">SERVICES</NuxtLink>
            </li>
            <li>
              <NuxtLink class="NuxtLink" to="/peopleSay">WHAT PEOPLE SAY?</NuxtLink>
            </li>
            <li>
              <NuxtLink class="NuxtLink" to="/faq">FAQ</NuxtLink>
            </li>
            <li>
              <NuxtLink class="NuxtLink" to="/contact">CONTACT</NuxtLink>
            </li>
          </ul>
        </nav>
      </v-navigation-drawer>
    </div>
    <div class="goto">
      <v-app-bar-nav-icon
        @click="drawer = !drawer"
        style="
        position: fixed;
        top: 20px;
        right: 20px;
        z-index: 2000;
        font-size: 40px!important;
"
        class="navIcon"
      ></v-app-bar-nav-icon>

      <v-navigation-drawer
        v-model="drawer"
        class="main-div"
        width="500px"
        fixed
        right
        app
      >
        <nav class="wrapper">
          <ul class="padding-top">
            <li>
              <div class="NuxtLink" @click="routeclick('#home')">Home</div>
            </li>
            <li>
              <div class="NuxtLink" @click="routeclick('#about')">About</div>
            </li>
            <li>
              <div class="NuxtLink" @click="routeclick('#services')">SERVICES</div>
            </li>
            <li>
              <div class="NuxtLink" @click="routeclick('#peopleSay')">WHAT PEOPLE SAY?</div>
            </li>
            <li>
              <div class="NuxtLink"  @click="routeclick('#faq')">FAQ</div>
            </li>
            <li>
              <div class="NuxtLink" @click="routeclick('#contact')">CONTACT</div>
            </li>
          </ul>
        </nav>
      </v-navigation-drawer>
    </div>

    <v-window class="scroll1">
      <home id="home"/>
      <about id="about"/>
      <services id="services"/>
      <people-say id="peopleSay"/>
      <faq id="faq"/>
      <contact id="contact"/>

    </v-window>

  </v-app>
</template>

<script>
import About from "~/pages/about"
import Faq from "~/pages/faq";
import Contact from "~/pages/contact";
import Home from "~/pages/home";
import Services from "~/pages/services";
import PeopleSay from "~/pages/peopleSay";

export default {
  components: {PeopleSay, Services, Home, About, Faq, Contact},
  data() {
    return {
      fixed: false,
      drawer: false,
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',
      index: 0,
      routes: [
        'home', 'about', 'faq', 'contact', 'peopleSay', 'services'
      ]
    }
  },
  methods: {
    nextRouting() {
      for (let i = 0; i < this.routes.length; i++) {
        this.index++
        if (this.index === this.routes.length - 1) {
          this.index = 0
        }
      }
    },
    routeclick(route){
      this.$vuetify.goTo(route)
    }
  }
}
</script>
<style>
.scroll1 {
  display: none;
}

.goto {
  display: none;
}

@media (max-width: 1300px) {
  ul {
    list-style-type: none;
  }

  .routing {
    display: none;
  }

  .goto {
    display: block;
  }

  li {
    margin: 0 0.5rem;
    padding: 0.25rem;
    font-size: 1.2rem;
  }

  .wrapper {
    transition: all 0.5s ease-in;
    background-color: grey;
    position: absolute;
    padding: 100px 0;
    width: 100%;
    height: 100%;
    left: -1000px;
  }

  .NuxtLink:hover {
    font-size: 120%;
  }

  .NuxtLink {
    text-align: center;
    padding-bottom: 20px;
    text-decoration: none !important;
    display: table;
    table-layout: fixed;
    width: 100%;
    color: #ffffff !important;

  }

  .wrapper:hover .NuxtLink {
    transition: all 0.1s ease-in;
    height: 100%;
    width: 100%;
  }

  .main-div {
    background-image: url("https://www.pandasecurity.com/en/mediacenter/src/uploads/2013/11/pandasecurity-facebook-photo-privacy.jpg");
    overflow: hidden;
    background-repeat: no-repeat;
    background-size: cover;
  }

  .btnn {
    position: fixed;
    right: 470px;
    z-index: 1000;
    top: 450px;
    color: lightcoral !important;
    background-color: white !important;


  }

  .main-div:hover .wrapper {
    transition: all 0.3s ease-in;
    background-color: grey;
    position: absolute;
    width: 100%;
    height: 100%;
    opacity: 0.8;
    left: 0;
    background-size: cover !important;
  }


  .v-card--reveal {
    align-items: center;
    bottom: 0;
    justify-content: center;
    opacity: 0.5;
    width: 100%;
  }


  .page-enter, .page-leave-active {
    opacity: 0;
    transform: translateX(4em);
  }

  .page-enter-active, .page-leave-active {
    transition: all 0.5s ease;
  }


  .navIcon {
    display: none;
  }

  .padding-top {
    padding: 200px 0;
  }

  .scroll1 {
    display: block;
  }

  .scroll2 {
    display: none;
  }
}

</style>
