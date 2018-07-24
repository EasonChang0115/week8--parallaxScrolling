<template>
  <div class="done">
    <div class="right" >
      <div class="content" :style="{display: selected === 0 ? '' : 'none'}">
        <div class="title">ALL DONE!</div>
        <div class="sub-title-2">Keep scrolling to show the result</div>
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
@import '../style/components/done.scss';
</style>
