<template>
  <div>
    <div class="score">
      <h1>{{ teamScore.teamName }}</h1>
      <br>
      <h2>{{ teamScore.score }}</h2>
    </div>
    <div class="buttomScore">
      <increase-and-decrease-score :team-score="teamScore" :increase-score="increaseScore" :decrease-score="decreaseScore" :index="index"></increase-and-decrease-score>
    </div>
  </div>
</template>

<script>
import IncreaseAndDecreaseScore from './IncreaseAndDecreaseScore'
export default {
  props: ['teamScore', 'increaseScore', 'decreaseScore', 'index'],
  components: {
    IncreaseAndDecreaseScore
  }
}
</script>

<style scoped>
h1 {
  color: #42b983;
}

.score {
  width: 300px;
  height: 250px;
  border: 5px solid #333;
}

.buttomScore{
  padding-top: 20px;
  width: 300px;
  height: 150px;
  border-top: none;
  border-left: 5px solid #333;
  border-right: 5px solid #333;
  border-bottom: 5px solid #333;
}
</style>
