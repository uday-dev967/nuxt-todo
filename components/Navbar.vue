<template>
  <div class="nav-bar">
    <v-app-bar color="deep-purple accent-4" dense dark>
      <NuxtLink to="/" class="app-title">
        <v-toolbar-title class="white--text">Vuex Todo</v-toolbar-title>
      </NuxtLink>

      <v-spacer></v-spacer>

      <input
        v-model="searchInput"
        type="text"
        class="search-field"
        placeholder="Search Todo"
      />
      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
      <NuxtLink to="/create">
        <v-btn icon>
          <v-icon>mdi-plus</v-icon>
        </v-btn>
      </NuxtLink>
      <v-btn icon>
        <v-icon>mdi-logout</v-icon>
      </v-btn>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  name: 'NavBar',
  data() {
    return {
      searchInput: '',
    }
  },
  methods: {},
}
</script>
<style>
.nav-bar {
  position: fixed;
  top: 0px;
  left: 0px;
  width: 100vw;
  z-index: 100;
}
.app-title {
  font-family: 'Montserrat', sans-serif;
  font-weight: 700;
  font-size: 1.5em;
  color: #39b982;
  text-decoration: none;
}
.search-field {
  background-color: #fff;
  outline: none;
  color: #000000;
  width: 400px;
  padding: 2px;
  border-radius: 5px;
  padding-left: 15px;
}
</style>
