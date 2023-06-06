<template>
  <!-- Start Blog 
      ============================================= -->
  <div
    id="blog"
    class="blog-style-one-area blog-area default-padding-top bottom-less mb-5 pb-5"
  >
    <div class="container">
      <div class="row">
        <div class="col-lg-8 offset-lg-2">
          <div class="site-heading text-center">
            <h4 class="sub-title">News</h4>
            <h2 class="title">Latest from blog</h2>
            <div class="devider"></div>
          </div>
        </div>
      </div>
    </div>
    <div class="container">
      <div class="row">
        <!-- Single item -->
        <BlogItem v-for="item in paginatedItems" :item="item" />
        <!-- End Single item -->
      </div>
      <div class="pagination">
        <button @click="previousPage" :disabled="currentPage === 1" class="btn-class">Previous</button>
        <button @click="nextPage" :disabled="currentPage === totalPages" class="btn-class">Next</button>
      </div>
    </div>

    <!-- Start Blog Single Modal -->
    <!-- End Blog Single Modal -->
    <BlogModal v-for="modal in respModal" :modal="modal" />
  </div>
  <!-- End Blog -->
</template>

<script setup>
import BlogItem from "../components/BlogSingleItem.vue";
import BlogModal from "../components/BlogSingleModal.vue";
import BlogJSON from "../assets/json/blog.json";
import BlogModalJSON from "../assets/json/blogmodal.json";

import { ref, onUpdated, watchEffect, reactive } from "vue";
import { computed } from "vue";

const response = ref(null);
const respModal = ref(null);
const currentPage = ref(1);
const itemsPerPage = 3; // Cambia este valor según tus necesidades

response.value = BlogJSON.reverse();
respModal.value = BlogModalJSON;

const paginatedItems = computed(() => {
  const start = (currentPage.value - 1) * itemsPerPage;
  const end = start + itemsPerPage;
  return response.value.slice(start, end);
});


const totalPages = computed(() => Math.ceil(response.value.length / itemsPerPage));

function previousPage() {
  if (currentPage.value > 1) {
    currentPage.value--;
  }
}

function nextPage() {
  if (currentPage.value < totalPages.value) {
    currentPage.value++;
  }
}
</script>

<style scoped>
.btn-class {
  background-color: #FF014F;
  width: 100px;
  color:whitesmoke;
  border-radius: 10px;
  border-color: #FF014F;
  
}

.btn-class:disabled {
  background-color:  #ff014d88;
}
</style>

