<template>
  <v-app>
    <!--<img src="component/img/m.jpg" /> -->
    <v-navigation-drawer
      v-model="drawer"
      fixed
      app
      style="
        background-image: url(https://i.pinimg.com/originals/ed/36/70/ed3670dd33f56f1fe312669538d52c9c.jpg);
      "
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      fixed
      app
      style="
        background-image: url(https://i.pinimg.com/originals/ed/36/70/ed3670dd33f56f1fe312669538d52c9c.jpg);
      "
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />

      <v-toolbar-title v-text="title" />
      <v-spacer />
      <!-- <nuxt-link to="/">Welcome </nuxt-link>
      <v-btn depressed color="primary" to="/inspire"> Inspire </v-btn>
      <v-btn class="ma-2" outlined color="indigo" to="/profile">
        Profile
      </v-btn>-->
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer
      style="
        background-image: url(https://i.pinimg.com/originals/ed/36/70/ed3670dd33f56f1fe312669538d52c9c.jpg);
      "
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'ARAYA TARIN',
          to: '/',
        },
        {
          icon: 'mdi-owl',
          title: 'Inspire',
          to: '/inspire',
        },
        {
          icon: 'mdi-language-go',
          title: 'Profile',
          to: '/Profile',
        },
        {
          icon: 'mdi-shopping',
          title: 'Shop',
          to: '/Shop',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: '🦄 𝔘𝔫𝔦𝔠𝔬𝔫 𝔊𝔦𝔣 🌈🌼',
    }
  },
}
</script>
<style>
#app {
  background-image: url(https://i.pinimg.com/originals/35/f2/a5/35f2a54da02f0cefb0bc6e13b6c8f310.jpg);
  background-size: mode;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #3a0414;
  margin-top: 60px;
}
</style>
