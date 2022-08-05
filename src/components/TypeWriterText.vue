<template>
  <p class="title">Hello World!</p>
  -------------------------------------------------
  <p class="name">I'm Surya Sonar</p>
  <vue-typed-js :strings="['First text', 'Second Text']">
    <h1 class="typing"></h1>
  </vue-typed-js>
</template>
<script>
export default {
  name: "TypeWriterText",
  component: {},
  data() {
    return {};
  },
  methods: {},
};
</script>

<style scoped>
* {
  box-sizing: border-box;
}
body {
  font-family: "Trebuchet MS", "Lucida Sans Unicode", sans-serif;
}
.title {
  color: rgb(255 255 255 / 80%);
  font-size: 30px;
  width: 418px;
  overflow: hidden;
  white-space: nowrap;
  animation: control-width-title 3s steps(12) 1s both, blink 0.5s infinite;
}

@keyframes control-width-title {
  from {
    width: 0;
  }
  to {
    width: 180px;
  }
}
.name {
  color: rgb(255 255 255 / 80%);
  font-size: 30px;
  width: 418px; /* You Can Use 28ch */
  /* margin: 30px auto; */
  overflow: hidden;
  white-space: nowrap;
  animation: control-width-name 3s steps(15) 5s both;
}
@keyframes control-width-name {
  from {
    width: 0;
  }
  to {
    width: 230px;
  }
}
</style>
