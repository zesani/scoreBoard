<template>
  <div>
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
</style>
