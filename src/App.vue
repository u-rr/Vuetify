<template>
  <div id="app">
    <v-toolbar class="red lighten-3">
      <v-toolbar-side-icon></v-toolbar-side-icon>
      <v-toolbar-title >ゆーるるのポートフォリオサイト</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn flat>ゆーるるについて</v-btn>
        <v-btn flat>Works</v-btn>
        <v-btn flat>お問い合わせ</v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
    <v-footer id="footer" dark height="auto">
      <v-card　class="flex" flat　tile>
        <v-card-title class="red lighten-3">
          <strong class="subheading">Get connected with us on social networks!</strong>

          <v-spacer></v-spacer>

          <v-btn
            v-for="icon in icons"
            :key="icon"
            class="mx-3"
            dark
            icon
          >
            <v-icon size="24px">{{ icon }}</v-icon>
          </v-btn>
        </v-card-title>

        <v-card-actions class="grey darken-3 justify-center">
          &copy;2019　 <strong>ゆーるるのポートフォリオサイト</strong>
        </v-card-actions>
      </v-card>
    </v-footer>
  </div>
</template>

<script>
  export default {
    data: () => ({
      icons: [
        'fab fa-facebook',
        'fab fa-twitter',
        'fab fa-linkedin',
        'fab fa-instagram'
      ]
    })
  }
</script>

<style>
  #footer {
    position: absolute;
    left: 0;
    bottom: 0;
    width: 100%;
    height: 100px;
  }
</style>