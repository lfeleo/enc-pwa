<template>
  <div id="app">
    <md-toolbar color="primary" class="expanded-toolbar">
      <span class="enc">
        <md-button> <router-link to="/">{{titre}} </router-link> </md-button>
        <md-button> <router-link to="/"><md-icon>home</md-icon> </router-link> </md-button>
      </span>

      <md-menu md-direction="bottom-start">
        <md-button md-menu-trigger> <md-icon> menu </md-icon></md-button>
        <md-menu-content>
          <md-menu-item> <router-link to="/"> Accueil </router-link></md-menu-item>
          <md-menu-item> <router-link to="/recherche"> Recherche </router-link></md-menu-item>
        </md-menu-content>
      </md-menu>
    </md-toolbar>
    <router-view/>
  </div>
</template>

<script lang="ts">
  import Vue from 'vue'
  export default class App extends Vue {
    titre ="Recherche de films";
  }
</script>

<style>
  #app{
    font-family: 'Gill Sans Ultra Bold';
  }

  .enc {
    flex:1;
    text-align: left;
  }

  h1{

    text-align: center;
  }

</style>