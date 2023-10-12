<template>
  <v-app dark>
    <nuxt />
    <nav-bar />
  </v-app>
</template>

<script>
import Navbar from '~/components/Navbar.vue'
export default {
  name: 'DefaultLayout',
  components: {
    'nav-bar': Navbar,
  },
  head() {
    return {
      titleTemplate: '%s - Todos App',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Where you can organize all your Tasks',
        },
      ],
    }
  },
}
</script>
