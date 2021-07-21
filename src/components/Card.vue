<template>
  <div>
    <h3>
      Card #{{cid}}
    </h3>
    <div v-if="loading">
      <h3>Loading Card...</h3>
    </div>
    <div v-else>
      Card Contents
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cid: 0,
      loading: false
    }
  },
  watch: {
    '$route': {
      handler: 'fetchData',
      immediate: true
    }
  },
  methods: {
    fetchData() {
      this.loading = true;
      setTimeout(() => {
        this.cid = this.$route.params.cid;
        this.loading = false;
      }, 600);
    }
  }
}
</script>

<style>

</style>