<template>
  <div>
    <a href="/" @click.prevent="$emit('click')">
      <h4>Finalmente eu consegui</h4>
    </a>
  </div>
</template>

<script>
export default {
  name: "about",
};
</script>

<style scoped>
h4 {
  color: blue;
}
</style>
