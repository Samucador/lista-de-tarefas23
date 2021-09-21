<template>
  <header>
      <h1>{{ valor }}</h1>
  </header>
</template>

<script>
export default {
  props: ["valor"],
}
</script>

<style scoped>
header {
  height: 50px;
  display: flex;
  width: 100%;
  background-color: darkslateblue;
  font-size: 15px;
  color: rgb(121, 246, 255);
  justify-content: center; 
  margin-top: -20px;
  padding: 10px;
}

</style>