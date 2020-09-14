<template>
  <header>
    <a href="/" @click.prevent="$emit('click')">
      <img src="../assets/logo.png" alt="Vue" />
      <h1>A tentação é semelhante a dor</h1>
    </a>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
h1 {
  font-size: 20px;
}
</style>