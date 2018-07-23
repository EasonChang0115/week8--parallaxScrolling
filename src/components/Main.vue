<template>
  <div class="main">
    <keep-alive>
      <component :is="stepMap[nowStep]" @my-chose="myChose"></component>
    </keep-alive>
  </div>
</template>

<script>
import HomePage from './HomePage';
import Question1 from './Question1';
import Question2 from './Question2';

export default {
  name: 'Main',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      stepMap: {
        1: 'HomePage',
        2: 'Question1',
        3: 'Question2'
      },
      nowStep: 1,
      question: 0,
      selectedArray: ['', '', '']
    };
  },
  mounted() {
    setTimeout(() => {
      this.nowStep = 2;
    }, 8000);
  },
  components: {
    HomePage,
    Question1,
    Question2
  },
  methods: {
    myChose(data) {
      this.selectedArray[this.question] = data;
      this.nowStep += 1;
      this.question += 1;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='scss'>
@import '../style/components/main.scss';
</style>
