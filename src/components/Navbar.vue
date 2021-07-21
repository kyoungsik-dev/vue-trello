<template>
  <header>
    <router-link to="/">Home</router-link>
    <router-link to="/login">Login</router-link>
  </header>
</template>

<script>
export default {

}
</script>

<style lang="scss">
header {
  height: 170px;
  padding: 30px;
  color: #fff;
  background-color: #2e2e2e;
  text-align: center;
  a {
    font-weight: 500;
    color: #fff;
    text-decoration: none;
    &:hover {
      color: #888;
    }
  }
}
</style>