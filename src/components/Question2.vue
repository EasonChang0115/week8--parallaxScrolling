<template>
  <div class="question-two">
    <div class="left" :class="selected === 0 ? '' : 'outAnimation'">
      <div class="block" :style="{display: selected === 0 ? '' : 'none'}">
        <div class="square"></div>
        <div class="triangle"></div>
        <div class="circle"></div>
      </div>
    </div>
    <div class="right fadeIn" >
      <div class="content" :style="{display: selected === 0 ? '' : 'none'}">
        <div class="title">Q2</div>
        <div class="sub-title">Imagine you’re almost late, but totally lost at a forked road. Which way do you prefer to go?</div>
        <div class="description">Choose the answer appeared in your mind instantly</div>
        <div class="button-group">
          <button @click="btnClick(1)">The left one</button>
          <button @click="btnClick(2)">The right one</button>
          <button @click="btnClick(3)">Open Google map</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Question2',
  data () {
    return {
      msg: 'Question2',
      selected: 0
    };
  },
  methods: {
    btnClick(option) {
      this.selected = option;
      this.$emit('my-chose', this.selected);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='scss'>
@import '../style/components/question-two.scss';
</style>
