<template>
  <LayoutView>
    <div
      class="col-lg-9 px-lg-4 pt-2 overflow-auto mainPanel d-flex align-items-center animate__animated animate__zoomIn"
    >
      <div class="row">
        <div class="col-lg-10 offset-lg-1 text-white">
          <div class="row">
            <div class="col-lg-3 col-md-6 p-0 d-flex align-items-center">
              <img
                src="/images/aboutProfile.jpg"
                alt=""
                class="rounded aboutProfile img-fluid animate__animated animate__zoomIn" 
              />
            </div>
            <div class="col-lg-8 col-md-6 ms-md-5">
              <span class="d-block text-white little">
                <small>A little bit</small>
              </span>
              <span class="d-block text-white fw-bold fs-2">About Me</span>
              <span class="d-block mb-3 text-success"> Web Developer </span>
              <p class="d-block text-white little">
                Hi there! I'm
                <span class="text-success">Thurein Htet</span> , a passionate
                and detail-oriented web developer with a solid foundation in
                front-end and back-end technologies. My journey into the world
                of web development is about
                <span class="text-success"> 1&nbsp;&frac12; years </span> until.
                Since then, I've been on a continuous learning path, studying
                ahead of the latest technologies and frameworks. Each project is
                an opportunity for me to push forward.
              </p>

              <span class="d-block text-white fw-bold fs-2 mt-5 mb-1">
                Contact
              </span>
              <span class="d-block text-white">
                <i class="fa-solid fa-phone me-2"></i>
                <small class="fw-thin">+959774999855</small>
              </span>
              <span class="d-block text-white">
                <i class="fa-solid fa-envelope me-2"></i>
                <small class="fw-thin">thureinhtet653@gmail.com</small>
              </span>
              <span class="d-block text-white">
                <i class="fa-solid fa-map-location-dot me-2"></i>
                <small class="fw-thin">
                  No.(11) Quarter, 2nd Street, Pakokku Township, Magway Region,
                  Myanmar
                </small>
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </LayoutView>
</template>

<script>
import LayoutView from "./LayoutView.vue";
export default {
  name: "AboutView",
  components: {
    LayoutView,
  },
};
</script>
