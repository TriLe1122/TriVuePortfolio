<template>
  <section id="contact" class="py-6 ">
    <div class="container gap-5">
      <div class="row">
        <div class="col-md-12 ">
          <p class="display-3 font-1 text-light">Get In Touch</p>
        </div>
      </div>

      <div class="row justify-content-center">
        <div class="col-md-8 text-center">

          <!-- <p class="font-2 fs-5 text-light ">
             I'm open to hire and looking for new opportunities to contribute to a worthwhile vision. The best way to get in touch with me is by phone, so don't hesitate to give me a call. I look forward to discussing how we can work together!
          </p> -->
        </div>
        <div class="col-md-6 d-flex justify-content-around">
          <a href="mailto:letrin93e@gmail.com" target="_blank"><button class="btn bg-transparent fs-1 font-1 ">
            <img src="https://cdn-icons-png.flaticon.com/512/732/732200.png" alt="Gmail Icon" title="Gmail Icon" width="100" height="100">
          </button></a>
          <a href="tel:2088630510" target="_blank">  <button class="btn bg-transparent fs-1 font-1 ">
            <img src="https://cdn-icons-png.flaticon.com/512/2936/2936151.png" alt="Phone Icon" title="Phone Icon" width="100" height="100">
          </button></a>
          <a href="https://www.linkedin.com/in/tri-le1122/" target="_blank"> <button class="btn bg-transparent fs-1 font-1 ">
              <img src="https://cdn-icons-png.flaticon.com/512/220/220343.png" alt="Phone Icon" title="Linkedin Icon" width="100"
                height="100">
            </button></a>

        </div>
      </div>


    </div>

  </section>
</template>

<script>
import { onMounted, ref, watchEffect } from "vue";



export default {
  props: {},
  setup(props) {
    const editable = ref({});
    return {
      editable,
    };
  },
  components: { },
};
</script>

<style lang="scss" scoped>


.my-6 {
  margin-top: 8rem;
  margin-bottom: 15rem;
}
.py-6 {
  padding-top: 5rem;
  padding-bottom: 5rem;
}





</style>
