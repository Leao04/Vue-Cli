<template>
  <div class="hello"></div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
};
</script>

<style scoped>
h1 {
  margin: 40px 0 0;
  font-size: 40px;
}

h2 {
  color: blue;
  font-size: 40px;
  margin: 40px 0 0;
}

ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: red;
  text-decoration: none;
}
</style>
