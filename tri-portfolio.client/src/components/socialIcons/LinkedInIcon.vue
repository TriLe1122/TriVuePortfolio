<template>
  <a href="https://www.linkedin.com/in/tri-le1122/" target="_blank" class="">
    <i class="mdi mdi-linkedin fs-3 text-light" title="Github"></i>
  </a>
</template>

<script>
export default {
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
i {
  transition: all 0.5s ease-out;
  @media only screen and (max-width: 768px) {
    font-size: 4rem!important;
  }
}
i:hover {
  color: turquoise !important;
}

a:hover {
  transform: translateY(-5px);
  transition: all 0.5s ease-out;
}
a {
  transition: all 0.5s ease-out;
}
</style>
