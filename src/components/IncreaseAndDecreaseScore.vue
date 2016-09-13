<template>
  <div class="buttomScore">
    <button type="button" class="btn btn-success" @click="increaseScore(index,1)">+1</button>
    <button type="button" class="btn btn-success" @click="increaseScore(index,2)">+2</button>
    <button type="button" class="btn btn-success" @click="increaseScore(index,3)">+3</button>
    <br><br>
    <button type="button" class="btn btn-danger" @click="decreaseScore(index,1)">-1</button>
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
