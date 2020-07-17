<template>
  <van-sticky>
    <van-nav-bar
      :title="title"
      right-text="..."
      left-arrow
      @click-left="$emit('navLeft')"
      @click-right="$emit('navRight')"
    />
  </van-sticky>
</template>

<script>
import { Sticky, NavBar } from 'vant'
export default {
  name: 'Navbar',
  components: {
    [Sticky.name]: Sticky,
    [NavBar.name]: NavBar
  },
  props: {
    title: {
      default: '导航栏',
      type: String,
      required: true
    }
  },
  data () {
    return {
    }
  },
  methods: {
    onClickLeft () {
    },
    onClickRight () {
    }
  }
}
</script>

<style scoped>

</style>
