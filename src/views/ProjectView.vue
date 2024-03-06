<template>
  <LayoutView>
    <div class="col-9 px-4 pt-2 overflow-auto mainPanel">
      <div class="row p-2">
        <div class="col">
          <span class="text-white fs-2">All Projects</span>
        </div>

        <!-- SearchBox -->
        <div
          class="col-3 p-0 rounded searchBoxFrame d-flex justify-content-end align-items-center"
        >
          <input
            type="search"
            class="w-100 rounded p-2 searchBox"
            placeholder="Search projects....."
            v-model="searchValue"
          />
          <button class="btn text-white-50">
            <i class="fa-solid fa-magnifying-glass"></i>
          </button>
        </div>
        <!-- End SearchBox -->
      </div>
      <div class="row px-4 py-2 d-flex justify-content-center">
        <div
          class="projectCards col-5 rounded-3 my-3 mx-4 animate__animated animate__zoomIn"
          v-for="(projectName, index) in filteredProjects"
          :key="index"
        >
          <div class="row">
            <div class="col p-0 text-center">
              <img
                :src="projectName.image"
                alt=""
                class="projectImg rounded-top-2"
              />
            </div>
          </div>
          <div class="row mt-3 mb-1">
            <div class="col my-2 px-4">
              <span
                class="px-2 me-2 small rounded projectCategory"
                v-for="category in projectName.categoryLists"
                :key="category.id"
              >
                {{ category.name }}
              </span>
            </div>
          </div>
          <div class="row mb-4">
            <div class="col px-4 text-white">
              <span class="fs-4 text-capitalize certificateName">{{
                projectName.name
              }}</span>
              <a href="" target="_blank" class="text-white">
                <i
                  class="fa-solid fa-arrow-up-right-from-square fa-sm ms-5"
                ></i>
              </a>
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
  name: "ProjectView",

  components: {
    LayoutView,
  },
  
  data() {
    return {
      searchValue: "",
      projectNames: [
        {
          id: 1,
          name: "academic center",
          image: require("/public/images/featuredPhoto.png"),
          categoryLists: [
            { id: 1, name: "Laravel" },
            { id: 2, name: "Vue.js" },
            { id: 3, name: "Css" },
            { id: 4, name: "Bootstrap" },
            { id: 5, name: "Api" },
            { id: 6, name: "Animate.css" },
          ],
        },
      ],
    };
  },

  computed: {
    filteredProjects() {
      return this.projectNames.filter((projects) => {
        return (
          projects.name.toLowerCase().indexOf(this.searchValue.toLowerCase()) !=
          -1
        );
      });
    },
  },
};
</script>
