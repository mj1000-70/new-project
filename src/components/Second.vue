<template>
<h1>Second</h1>
  <h2>{{header}}</h2>
  <p>{{text}}</p>

</template>

<script>
export default {
props:['header','text'],
  name: "SecondView"
}
</script>

<style scoped>

</style>