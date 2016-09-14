<template>
  <div id="app">
    <div class="box" v-for="teamScore in teamScores">
      <board :team-score="teamScore"></board><br>
      <increase-score :increase-score="increaseScore" :index="$index"></increase-score><br>
      <decrease-score :decrease-score="decreaseScore" :index="$index"></decrease-score>
    </div>
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous">
  </div>
</template>

<script>
import Board from './components/Board'
import IncreaseScore from './components/IncreaseScore'
import DecreaseScore from './components/DecreaseScore'
export default {
  components: {
    Board,
    IncreaseScore,
    DecreaseScore
  },
  data () {
    return {
      teamScores: [{
        teamName: 'Home',
        score: 0
      }, {
        teamName: 'Away',
        score: 0
      }]
    }
  },
  methods: {
    increaseScore: function (index, point) {
      this.teamScores[index].score += point
    },
    decreaseScore: function (index, point) {
      if (this.teamScores[index].score > 0) {
        this.teamScores[index].score -= point
      }
    }
  }
}
</script>

<style>
html {
  height: 100%;
}

body {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}

#app {
  color: #2c3e50;
  margin-top: 0px;
  max-width: 900px;
  font-family: Source Sans Pro, Helvetica, sans-serif;
  text-align: center;
}

.box {
  display: inline-block;
  width: 300px;
  height: 400px;
  margin: 1px;
  border: 5px solid #333;
}

</style>
