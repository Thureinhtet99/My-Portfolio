<template>
  <div class="container-fluid">
    <div class="row">
      <!-- Side Panel -->
      <div
        class="col-lg-3 col-md-4 col-sm-6 d-flex flex-column justify-content-between sidePanel"
      >
        <div class="row mt-5">
          <div class="col-12 text-center">
            <img
              src="images/myProfile.jpg"
              alt=""
              class="object-fit-cover myProfile"
            />
            <h2 class="text-white">Thurein Htet</h2>
            <p class="text-white">Web Developer</p>
          </div>
        </div>

        <div class="row">
          <div class="col ms-4 ps-5">
            <nav class="mb-4">
              <router-link
                class="text-white text-decoration-none fs-6 navLink"
                to="/"
              >
                <i class="fa-solid fa-house me-3"></i>Dashboard
              </router-link>
            </nav>
            <nav class="mb-4">
              <router-link
                class="text-white text-decoration-none fs-6 navLink"
                to="/projects"
              >
                <i class="fa-solid fa-diagram-project me-3"></i>Projects
              </router-link>
            </nav>
            <nav class="mb-4">
              <router-link
                class="text-white text-decoration-none fs-6 navLink"
                to="/certificate"
              >
                <i class="fa-solid fa-certificate me-3"></i>Certificates
              </router-link>
            </nav>
            <nav class="mb-4">
              <router-link
                class="text-white text-decoration-none fs-6 navLink"
                to="/about"
              >
                <i class="fa-solid fa-user me-3"></i>About
              </router-link>
            </nav>
          </div>
        </div>

        <footer>
          <div class="row text-center mb-2 p-2">
            <div class="col-6 d-flex flex-column align-items-start gap-2">
              <a
                href="https://www.facebook.com/profile.php?id=100010238821531"
                title="Facebook"
                class="text-white text-decoration-none"
                target="_blank"
              >
                <i class="fa-brands fa-facebook me-2"></i>
                <span class="small">Facebook</span>
              </a>
              <a
                href="https://github.com/Thureinhtet99"
                title="Github"
                target="_blank"
                class="text-white text-decoration-none"
              >
                <i class="fa-brands fa-github me-2"></i
                ><span class="small">Github</span>
              </a>
            </div>
            <div class="col-6 d-flex flex-column align-items-start gap-2">
              <a
                href="https://www.linkedin.com/in/thureinhtet99/"
                title="Linkedin"
                target="_blank"
                class="text-white text-decoration-none"
              >
                <i class="fa-brands fa-linkedin me-2"></i
                ><span class="small">Linkedin</span>
              </a>
              <a
                download="My Resume"
                href="/images/CV resume form.pdf"
                title="Download CV"
                class="text-decoration-none text-white"
                data-bs-toggle="tooltip"
                data-bs-placement="top"
                data-bs-custom-class="custom-tooltip"
                data-bs-title="This top tooltip is themed via CSS variables."
              >
                <i class="fa-solid fa-download me-2"></i
                ><span class="small">Download CV</span>
              </a>
            </div>
          </div>
        </footer>
      </div>
      <!-- End Side Panel -->

      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {};
</script>
