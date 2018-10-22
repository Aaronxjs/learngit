<template>
    <div :class="$style.home">
        <Header></Header>
        <Slider></Slider>
    </div>
</template>

<script>
import Header from '../public/header.vue'
import Slider from './hslider.vue'
export default {
  components: {
    Header,
    Slider
  }
}
</script>

<style lang="scss" module>
  @import '../../css/reset.scss';
  .home{
    color: red;
    font-size: 80px;
  }
</style>
