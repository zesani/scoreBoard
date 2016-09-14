<template>
  <div>
    <button type="button" class="btn btn-success" @click="increaseScore(index,1)">+1</button>
    <button type="button" class="btn btn-success" @click="increaseScore(index,2)">+2</button>
    <button type="button" class="btn btn-success" @click="increaseScore(index,3)">+3</button>
  </div>
</template>

<script>
export default {
  props: ['increaseScore', 'index']
}
</script>

<style scoped>
h1 {
  color: #42b983;
}

</style>
