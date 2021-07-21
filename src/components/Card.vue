<template>
  <div>
    <h3>
      Card #{{cid}}
    </h3>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cid: 1
    }
  },
  watch: {
    '$route'() {
      this.cid = this.$route.params.cid;
    }
  },
  created() {
    this.cid = this.$route.params.cid;
  }
}
</script>

<style>

</style>