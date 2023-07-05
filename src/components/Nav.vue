
<script>
export default {
  props: {
    isOpen: {
      type: Boolean,
      default: false,
    },
    handleOpenMenu: {
      type: Function,
      default: () => {},
    },
  },
  setup(props, { emit }) {
    return { props };
  },
};
</script>


<template>
  <div :class="['nav', { open: props.isOpen }]">
    <a @click="props.handleOpenMenu">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="h-5 w-5"
        viewBox="0 0 20 20"
        fill="currentColor"
      >
        <path
          fill-rule="evenodd"
          d="M10 18a8 8 0 100-16 8 8 0 000 16zM8.707 7.293a1 1 0 00-1.414 1.414L8.586 10l-1.293 1.293a1 1 0 101.414 1.414L10 11.414l1.293 1.293a1 1 0 001.414-1.414L11.414 10l1.293-1.293a1 1 0 00-1.414-1.414L10 8.586 8.707 7.293z"
          clip-rule="evenodd"
        />
      </svg>
    </a>
  </div>
</template>

<style lang="scss" scoped>
.nav {
  position: relative;
  width: 300px;
  height: 100vh;
  background: #fff;
  position: absolute;
  top: 0;
  right: -300px;
  transition: right 0.3s;
  &.open {
    right: 0;
  }
}
a {
  position: absolute;
  top: 10px;
  right: 10px;
  cursor: pointer;
  display: block;
  width: 50px;
  height: 50px;
  color: slategrey;
  transition: color 0.3s;
  &:hover {
    color: teal;
  }
}
</style>
