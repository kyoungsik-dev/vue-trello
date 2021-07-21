<template>
  <div>
    <h2>Board #{{bid}}</h2>
    <ul>
      <li v-for="idx in [1,2,3,4,5]" v-bind:key="idx" >
        <router-link :to="'/board/'+bid+'/card/'+idx">
          Card {{idx}}
        </router-link>
      </li>
    </ul>
    <hr />
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  data() {
    return {
      bid: 0
    }
  }, 
  created() {
    this.bid = this.$route.params.bid;
  }
}
</script>

<style>

</style>