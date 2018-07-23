<template>
  <div class="question-one">
    <div class="left fadeIn">
      <div class="content" :style="{display: selected === 0 ? '' : 'none'}">
        <div class="title">Q1</div>
        <div class="sub-title">If one day you get a gift that can change the rule of the world, which ability will you choose?</div>
        <div class="description">Choose the answer appeared in your mind instantly</div>
        <div class="button-group">
          <button @click="btnClick(1)">Destroy all humans in the world</button>
          <button @click="btnClick(2)">Make the war never happened</button>
          <button @click="btnClick(3)">You won’t get old and live forever</button>
        </div>
      </div>
    </div>
    <div class="right">
      <div class="block" :style="{display: selected === 0 ? '' : 'none'}">
        <div class="square"></div>
        <div class="triangle"></div>
        <div class="circle"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Question1',
  data () {
    return {
      msg: 'Question1',
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
@import '../style/components/question-one.scss';
</style>
