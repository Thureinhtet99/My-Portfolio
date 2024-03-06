<template>
  <LayoutView>
    <div class="col-lg-9 col-md-10 col-sm-12 px-4 pt-2 overflow-auto mainPanel">
      <div class="row p-2">
        <div class="col">
          <span class="text-white fs-2">My Certificates</span>
        </div>

        <!-- SearchBox -->
        <div
          class="col-lg-3 col-md-4 col-sm-6 p-0 rounded searchBoxFrame d-flex justify-content-end align-items-center"
        >
          <input
            type="search"
            class="w-100 rounded p-2 searchBox"
            placeholder="Search certificates....."
            v-model="searchValue"
          />
          <button class="btn text-white-50">
            <i class="fa-solid fa-magnifying-glass"></i>
          </button>
        </div>
        <!-- End SearchBox -->

        <div
          class="col-12 mb-5 d-flex flex-column align-items-center justify-content-center"
          v-for="(item, index) in searchCertificate"
          :key="index"
        >
          <!-- Cards -->
          <div class="card my-5 animate__animated animate__zoomIn">
            <img :src="item.image" width="100%" class="card-img-top" alt="" />
            <div class="card-body">
              <p class="fs-5 my-0 text-capitalize certificateName">
                {{ item.name }}
              </p>
            </div>
          </div>
          <!-- End Cards -->
        </div>
      </div>
    </div>
  </LayoutView>
</template>

<script>
import LayoutView from "./LayoutView.vue";
export default {
  name: "CertificateView",
  data() {
    return {
      searchValue: "",
      certificateList: [
        {
          id: 1,
          name: "fullstack developer course",
          image: require("/public/images/FDC-Certificate.jpg"),
        },
        {
          id: 2,
          name: "frontend (Laravel) + backend (Vue)",
          image: require("/public/images/Vue-JS-Certificate.jpg"),
        },
        {
          id: 3,
          name: "responsive web design",
          image: require("/public/images/Web-Design-Certificate.jpg"),
        },
        {
          id: 4,
          name: "web fundamentals",
          image: require("/public/images/hornbill.jpg"),
        },
      ],
    };
  },

  components: {
    LayoutView,
  },

  computed: {
    searchCertificate() {
      return this.certificateList.filter((certi) => {
        return (
          certi.name.toLowerCase().indexOf(this.searchValue.toLowerCase()) != -1
        );
      });
    },
  },
};
</script>
