<template>
  <div>
    <button type="button" class="btn btn-danger" @click="decreaseScore(index,1)">-1</button>
  </div>
</template>

<script>
export default {
  props: ['decreaseScore', 'index']
}
</script>

<style scoped>
h1 {
  color: #42b983;
}

</style>
