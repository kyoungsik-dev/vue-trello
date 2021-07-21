<template>
  <div>
    <h2>Board #{{bid}}</h2>
    <div v-if="loading">
      <h3>
        Loading Board...
      </h3>
    </div>
    <ul v-else>
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
      bid: 0,
      loading: false
    }
  }, 
  created() {
    this.fetchData();
  },
  methods: {
    fetchData() {
      this.loading = true;
      setTimeout(() => {
        this.bid = this.$route.params.bid;
        this.loading = false;
      }, 500);
    }
  }
}
</script>

<style>

</style>