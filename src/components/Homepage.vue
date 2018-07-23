<template>
  <div class="home-page">
    <div class="container">
      <div class="block"></div>
      <div class="circle"></div>
      <div class="triangle"></div>
      <div class="title-block">
        <div class="title">GEOMETRY PERSON</div>
        <div class="sub-title-2">find your core personality type in shapes!</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Homepage',
  data () {
    return {
      msg: 'Homepage'
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='scss'>
@import '../style/components/home-page.scss';
</style>
