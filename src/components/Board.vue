<template>
  <div>
    <div class="score">
      <h1>{{ teamScore.teamName }}</h1>
      <br>
      <h2>{{ teamScore.score }}</h2>
    </div>
  </div>
</template>

<script>
export default {
  props: ['teamScore', 'increaseScore', 'decreaseScore', 'index']
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

</style>
