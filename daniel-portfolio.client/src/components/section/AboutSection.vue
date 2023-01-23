<template>
  <section id="about" class="about py-5 mt-0 text-light font-1 bg-custom">
    <div class="container">
      <div class="d-flex justify-content-between">
        <div class="section-title display-3">
          <h1>About me</h1>
        </div>
      </div>

      <div class="row justify-content-center" ref="container">
        <div class="col-md-4 d-flex justify-content-center">
          <div class="card-container">
            <div class="image-card perspective-left">
              <div class="box box3">
                <div class="oddboxinner elevation-6"></div>
              </div>
            </div>
          </div>
        </div>

        <div
          class="col-lg-8 pt-4 pt-lg-0 content px-md-5 d-flex align-items-center"
        >




          <p
            v-motion-slide-visible-once-bottom
            :delay="300"
            class="px-md-5 font-2 text-start about-me-text long-paragraph"
          >
            I am Tri Le, a full stack developer with a demonstrated ability in problem-solving and critical thinking. I possess a
            solid foundation in both front and back-end development, and have a passion for discovering unique solutions to
            intricate issues.

            <br/>
            I am captivated by the intricacies of development and the design of programming architecture with a natural inclination towards problem-solving
            and a fervent desire to create seamless websites and applications with exceptional performance.

            <br/>
            I have a passion for back-end development and am proficient in utilizing technologies such as Node.js, Express,
            and SQL. I have a constant eagerness to learn and advance as a developer, and take pride in my ability to quickly adapt
            and acquire new technologies.
            <br/>
            I am a strong advocate that excellent software is constructed on a foundation of transparent communication and
            collaboration. I am committed to working with my team to achieve the highest quality outcome. I appreciate you taking
            the time to learn more about me. I eagerly anticipate the chance to collaborate with you and apply my skills and
            knowledge to your project.
          </p>
        </div>
      </div>

      <div class="row my-5 justify-content-center">
        <div class="col-md-6 text-center">
          <p class="font-1 fs-4 text-warning">Favorite playlist to code to</p>
          <iframe style="border-radius:12px"
            src="https://open.spotify.com/embed/playlist/4ANPW38qMEYQ3Z1mVLrtmm?utm_source=generator&theme=0" width="100%"
            height="352" frameBorder="0" allowfullscreen=""
            allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
        </div>
        <div class="col-md-6 text-center">
          <p class="font-1 fs-4 text-warning">Hobbies and Passions</p>
          <div class="d-md-flex justify-content-around p-2">
            <img
              src="https://upload.wikimedia.org/wikipedia/en/thumb/a/aa/Magic_the_gathering-card_back.jpg/220px-Magic_the_gathering-card_back.jpg"
              alt=""
              width="240"
              height="240"
              class="elevation-6 rounded mb-2 mb-md-0"
            />
            <img
              src="https://d99q83nas8cxh.cloudfront.net/wp-content/uploads/2019/02/the-base-mural-dark-nontransparent.png"
              alt=""
              width="240"
              height="240"
              class="elevation-6 rounded"
            />
          </div>
        </div>
      </div>
    </div>
    <!-- <BlockQuote/> -->
  </section>
</template>

<script>
import { computed } from "@vue/reactivity";
import { useParallax } from "@vueuse/core";
import { onMounted, ref, watchEffect } from "vue";
import ParallaxMouse from "../cardEffect/ParallaxMouse.vue";


export default {
  props: {},
  setup(props) {
    const editable = ref({});
    const container = ref(null);
    const { tilt, roll, source } = useParallax(container);

    // Use an intersection observer to call the typeWriter function when the element comes into view

    onMounted(() => {});

    watchEffect(() => {});

    return {
      editable,
      container,
    };
  },
  components: { ParallaxMouse},
};
</script>

<style lang="scss" scoped>
.bg-custom{
    background-image: url("../img/pexels.mp4");
}
.about-me-text {
  font-size: 1.25rem;
  //when screen is 768px OR LESS
  @media only screen and (max-width: 768px) {
    font-size: 1rem;
  }
}
.procreate-art {
  width: auto;
  height: 300px;
  cursor: pointer;
}

.procreate-art:hover {
  transform: scale(1.01);
  transition: all 0.5s ease;
}
.box {
background-image: url("../../assets/img/trile.jpg");
  border: solid black;
  border-color: black;
  background-position: center;
  background-size: cover;
}

.box3 {
  border-width: 5px 3px 3px 5px;
  border-radius: 95% 4% 97% 5%/4% 94% 3% 95%;
  transform: rotate(2deg);
}

.oddboxinner {
  height: 500px;
  margin: 15px;
  transform: rotate(-2deg);
  //when screen is 768px OR LESS
  @media only screen and (max-width: 768px) {
    height: 305px;
  }
}

.image-card {
  width: 440px;
  height: 560px;
  padding: 8px;
  border-radius: 1rem;
  background-position: center;
  background-size: cover;
  // background: url("https://images.pexels.com/photos/8482473/pexels-photo-8482473.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2");
  background-image: url("https://media4.giphy.com/media/NXEuPHCOiJujANVznL/giphy.gif?cid=ecf05e47fa6ifvzskbadjnmw5ejox6ihyzuuga7shom3snof&rid=giphy.gif&ct=g");
  box-shadow: rgba(0, 0, 0, 0.25) 0px 25px 50px -12px;
  //when screen is 768px OR LESS
  @media only screen and (max-width: 768px) {
    width: 240px;
    height: 360px;
  }
}

.perspective-left {
  transform: perspective(1500px) rotateY(15deg);
  transition: transform 1s ease 0s;
}

.perspective-left:hover {
  transform: perspective(3000px) rotateY(5deg);
}

.perspective-right {
  transform: perspective(1500px) rotateY(-15deg);
  transition: transform 1s ease 0s;
}

.perspective-right:hover {
  transform: perspective(3000px) rotateY(-5deg);
}
</style>
