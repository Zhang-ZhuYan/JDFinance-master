<template>
  <div id="app">
    <a-header></a-header>
    <a-swiper></a-swiper>
  </div>
</template>

<script>
import AHeader from './public/header'
import ASwiper from './public/swiper'
export default {
  name: 'app',
  components: {
    AHeader,
    ASwiper
  }
}
</script>
