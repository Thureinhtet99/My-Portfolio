<template>
  <LayoutView>
    <!-- Main Panel  -->
    <div
      class="col-lg-9 col-md-10 col-sm-12 parent mainPanel overflow-auto px-4 pt-4"
    >
      <div
        class="div1 py-4 d-flex flex-column justify-content-center align-items-center rounded-3 animate__animated animate__zoomIn"
      >
        <span class="fs-2 text-white"> 5 </span>
        <span class="text-white">
          <small>Projects</small>
        </span>
      </div>
      <div
        class="div2 py-4 px-3 d-flex text-center justify-content-center align-items-center rounded-3 animate__animated animate__zoomIn"
      >
        <span class="p-0 fs-5 text-white text-capitalize">
          {{ text }}
        </span>
      </div>
      <div
        class="div3 py-4 d-flex flex-column text-center justify-content-center align-items-center rounded-3 animate__animated animate__zoomIn"
      >
        <section class="">
          <span class="fs-2 text-white me-1"> 1 &nbsp;&frac12; </span>
          <span class="text-white">
            <small> Years </small>
          </span>
        </section>
        <span class="d-block text-white">Experience</span>
      </div>
      <div
        class="div4 py-4 rounded-3 d-flex flex-column text-center justify-content-center align-items-center animate__animated animate__zoomIn"
      >
        <span class="fs-2 text-white animate__animated animate__zoomIn">4</span>
        <span class="text-white">Certificates</span>
      </div>
      <div
        class="div5 px-4 d-flex flex-column justify-content-center rounded-3 animate__animated animate__zoomIn"
      >
        <span class="d-block fs-3 mb-2 text-white">
          Your passionate web developer
        </span>
        <span class="d-block">
          <small class="text-white-50">
            Passionate and detail-oriented web developer with a solid foundation
            in front-end and back-end technologies.
          </small>
        </span>
        <span class="mt-3">
          <nav>
            <router-link
              to="/about"
              class="text-decoration-none text-success viewAll"
            >
              Get in touch
            </router-link>
            <i
              class="fa-solid fa-angle-right text-primary fa-sm ms-1 text-success"
            ></i>
          </nav>
        </span>
      </div>
      <div
        class="div6 pt-4 d-flex flex-column justify-content-between align-items-center rounded-3 animate__animated animate__zoomIn"
      >
        <section class="text-center">
          <span class="d-block fs-3 text-white">Featured Projects</span>
          <span class="">
            <nav>
              <router-link
                to="/projects"
                class="text-decoration-none text-success viewAll"
              >
                View All
              </router-link>
              <i
                class="fa-solid fa-angle-right text-primary fa-sm ms-1 text-success"
              ></i>
            </nav>
          </span>
        </section>
        <img
          src="/images/featuredPhoto.png"
          alt=""
          class="mt-5 featuredImg rounded-top"
        />
      </div>
      <div
        class="div7 p-4 text-center rounded-3 animate__animated animate__zoomIn"
      >
        <span class="d-block text-center fs-3 text-white">Certificates</span>
        <span class="">
          <nav>
            <router-link
              to="/certificate"
              class="text-decoration-none text-success viewAll"
            >
              View All
            </router-link>
            <i
              class="fa-solid fa-angle-right text-primary fa-sm ms-1 text-success"
            ></i>
          </nav>
        </span>
        <section class="certificateBox mt-5">
          <section class="certi1">
            <a
              href="file:///D:/Web%20Development/eimg/eimg%20PDF/Professional-Web-Developer-2022.pdf"
              target="_blank"
            >
              <img
                src="/images/FDC-Certificate.jpg"
                alt=""
                class="certificateImg rounded"
              />
            </a>
          </section>
          <section class="certi2">
            <img
              src="/images/Vue-JS-Certificate.jpg"
              alt=""
              class="certificateImg rounded"
            />
          </section>
          <section class="certi3">
            <img
              src="/images/Web-Design-Certificate.jpg"
              alt=""
              class="certificateImg rounded"
            />
          </section>
          <section class="certi4"></section>
          <section class="certi5">
            <img
              src="/images/hornbill.jpg"
              alt=""
              class="certificateImg rounded"
            />
          </section>
          <section class="certi6"></section>
        </section>
      </div>
    </div>
  </LayoutView>
</template>

<script>
import LayoutView from "./LayoutView.vue";
export default {
  name: "HomeView",

  components: {
    LayoutView,
  },
  data() {
    return {
      careerList: ["full-stack webdeveloper"],
      careerWord: 0,
      careerLetter: 0,
      text: "",
    };
  },

  methods: {
    textChange() {
      this.careerLetter++;
      this.text = this.careerList[this.careerWord].slice(0, this.careerLetter);

      if (this.careerLetter === this.careerList[this.careerWord].length) {
        this.careerWord++;
        this.careerLetter = 0;

        if (this.careerWord === this.careerList.length) {
          this.careerWord = 0;
        }
      }

      setTimeout(() => {
        this.textChange();
      }, 200);
    },
  },

  mounted() {
    setTimeout(() => {
      this.textChange();
    }, 1000);
  },
};
</script>
