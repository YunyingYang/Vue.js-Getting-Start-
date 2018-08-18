<template>
  <div id="app">
    <div class="sports-field">
      <h1>{{ title }}</h1>
      <board :score="score" :miss="miss"></board>
      <goal></goal>
      <ball :image="src" @score="score ++" @miss="miss ++"></ball>
    </div>
  </div>
</template>

<script>
import Goal from './components/Goal.vue'
import Ball from './components/Ball.vue'
import Board from './components/Board.vue'

export default {
  components: {
    Goal,
    Ball,
    Board//这个很重要，一定要加
  }, 

  data () {
    return {
      score: 0,
      miss:0,
      status: '',
      title: "A little ball ball⚽️",
      goalClass: "something-great",
      src:'/static/soccer-ball.png'
    }
  },

  methods: {
    // shoot () { 
    //   const results = [
    //     'miss',
    //     'score'
    //   ]

    //   this.status = results[Math.floor(Math.random() * results.length)]

    //   setTimeout(() => {
    //     this.reset()
    //   }, 800)
    // },

    // reset () {
    //   this.status = 'reset'
    //   setTimeout(() => {
    //     this.status = ''
    //   }, 500)
    // },

    // imageSrc(){
    //   return '/static/soccer-ball.png'
    // }
  }
}
</script>

<style>
</style>
