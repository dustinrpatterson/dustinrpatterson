<template>
  <v-app>

    <v-toolbar
      app
      :clipped-left="clipped">
      <v-toolbar-title>
        <router-link to="/">
          <!-- TODO - make this clickable back to home, add an image -->
        </router-link>
        Dustin R. Patterson
      </v-toolbar-title>
      <v-spacer/>
      <v-toolbar-items>
        <v-btn
          v-for="navItem in navItems"
          :key="navItem"
          :to="navItem.link"
          router
          flat>{{ navItem.name }}</v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <v-content>
      <router-view/>
    </v-content>

    <v-footer
      :fixed="fixed"
      app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
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
