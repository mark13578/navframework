<script>
import { ref } from "vue";
import Header from "./components/Header.vue";
import Nav from "./components/Nav.vue";
export default {
  components: {
    Header,
    Nav,
  },
  setup() {
    const isOpen = ref(false);

    const handleOpenMenu = () => {
      isOpen.value = !isOpen.value;
    };

    return { isOpen, handleOpenMenu };
  },
};
</script>

<template>
  <Header :handleOpenMenu="handleOpenMenu" />
  <Nav :isOpen="isOpen" :handleOpenMenu="handleOpenMenu" />
</template>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
html,
body {
  width: 100%;
  height: 100%;
  background-color: slategrey;
  /* background-image: url("https://source.unsplash.com/user/erondu/1600x900"); */
  background-position: center;
  background-size: cover;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
