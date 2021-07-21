<template>
  <div id="app">
    <Navbar />
    <div class="container">
      <router-view></router-view>
    </div>
    <footer>
      Footer
    </footer>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';

export default {
  name: 'app',
  components: { Navbar },
  data () {
    return {
    }
  }
}
</script>

<style lang="scss">
body { margin: 0 }
footer {
  margin: 40px;
  padding-top: 20px;
  border-top: 1px solid #eee;
  text-align: center;
  font-size: 16px;
}
.container {
  padding: 20px;
}
</style>
