<template>
  <header>
    <Navbar class="fixed-top" id="nav" />
  </header>
  <main  class="bg-custom">
   
    <router-view />
  </main>
</template>

<script>
import { computed, onMounted } from "vue";
import { AppState } from "./AppState";
import Navbar from "./components/Navbar.vue";

export default {
  setup() {
    onMounted(() => {
    

      hideOnScrollTest("#nav");
   
    });

  

    function hideOnScrollTest(el) {
      let nav = document.querySelector(`${el}`);

      let prevScrollpos = window.scrollY;

      // console.log(nav);
      window.onscroll = function () {
        let currentScrollPos = window.scrollY;
        if (prevScrollpos > currentScrollPos) {
          nav.style.top = "0";
        } else {
          nav.style.top = "-62px";
        }
        prevScrollpos = currentScrollPos;
      };
    }

    return {
      appState: computed(() => AppState),
    };
  },
  components: { Navbar },
};
</script>
<style lang="scss">
@import "./assets/scss/main.scss";

.bg-custom{
background: rgb(201, 95, 28);
  background: linear-gradient(27deg, rgba(201, 95, 28, 1) 0%, rgba(121, 9, 58, 1) 46%, rgb(10, 10, 10) 85%);
// background-image: url("https://www.pixel4k.com/wp-content/uploads/2020/01/burning-colours-abstract-4k-a3-3840x2160-1.jpg");
// background-size: contain;
// background-attachment: fixed;
}

#nav {
  transition: all 0.5s ease-out;
}

:root {
  --main-height: calc(100vh - 64px);
}
</style>
