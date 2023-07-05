<script>
export default {
  props: {
    handleOpenMenu: {
      type: Function,
      default: () => {},
    },
  },
  setup(props) {
    return { props };
  },
};
</script>

<template>
  <header>
    <nav>
      <button @click="props.handleOpenMenu">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-5 w-5"
          viewBox="0 0 20 20"
          fill="currentColor"
        >
          <path
            fill-rule="evenodd"
            d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
            clip-rule="evenodd"
          />
        </svg>
      </button>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
header {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 55px;
  background-color: #4eb883;
  padding-left: 30px;
  nav {
    display: flex;
    justify-content: flex-start;
    height: 100%;
    button {
      cursor: pointer;
      display: flex;
      justify-content: center;
      align-items: center;
      width: 50px;
      height: 100%;
      font-size: 14px;
      margin-right: 10px;
      transition: background 0.1s;
      border: 0;
      background-color: rgba($color: #fff, $alpha: 0);
      color: #fff;
      &:hover {
        background-color: #35495d;
      }
    }
  }
}
</style>
