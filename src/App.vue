<template>
  <v-app>

    <v-toolbar app>
      <v-toolbar-title>
        <router-link to="/">
          <!-- TODO - make this clickable back to home, add an image -->
        </router-link>
        Dustin R. Patterson
      </v-toolbar-title>
      <v-spacer/>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn
          v-for="(navItem, index) in navItems"
          :key="index"
          :to="navItem.link"
          router
          flat>{{ navItem.name }}</v-btn>
      </v-toolbar-items>
      <v-toolbar-side-icon
        @click.stop="drawer = !drawer"
        class="hidden-md-and-up"/>
    </v-toolbar>
    <v-navigation-drawer
      temporary
      v-model="drawer"
      absolute
    >
      <v-list
        class="pt-0"
        dense>
        <v-list-tile
          v-for="(navItem, index) in NavItems"
          :key="index"
        >
          <v-list-tile-content>
            <v-list-tile-title>{{ navItem.name }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-content>
      <router-view/>
    </v-content>

    <v-footer
      fixed
      app
      class="px-2">
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      drawer: null,
      navItems: [
        {
          name: 'Portfolio',
          link: '/portfolio'
        },
        {
          name: 'Education',
          link: '/education'
        },
        {
          name: 'Experience',
          link: '/experience'
        },
        {
          name: 'About',
          link: '/about'
        },
        {
          name: 'Contact',
          link: '/contact'
        }
      ]
    }
  }
}
</script>
