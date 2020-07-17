<template>
  <div class="about">
    <h1 @click="change">{{ hi }}</h1>
    <h2>{{saiHi()}}</h2>
  </div>
</template>
<style scoped lang="scss">
</style>

<script>
export default {
  data () {
    return {
      hi: 'hello'
    }
  },
  computed: {
    saiHi () {
      return this.hi + ` world`
    }
  },
  methods: {}
}

</script>
