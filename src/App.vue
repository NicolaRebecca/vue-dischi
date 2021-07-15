<template>
  <div id="app">
    <Loader v-if="albums.length == 0" />
    <Header />
    <Main :albums='albums' />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import axios from "axios";
import Loader from "./components/Loader.vue"

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Loader
  },
  created () {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((result) => {
      this.albums = result.data.response;
    })
  },
  data() {
    return {
      albums: []
    }
  }
}
</script>

<style lang="scss">

</style>
