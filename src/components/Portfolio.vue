<script setup>
import SingleItem from "./PortfolioSingleItem.vue";
import SingleModal from "./PortfolioSingleModal.vue";
import { ref, onUpdated, watchEffect, reactive } from "vue";
import Portfolio from "../assets/json/portfolio.json";
import Modal from "../assets/json/modal.json";
import { computed } from "vue";
const response = ref(null);
const respModal = ref(null);
const currentPage = ref(1);
const itemsPerPage = 3; // Cambia este valor según tus necesidades

response.value = Portfolio.reverse();
respModal.value = Modal;


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

<template>
  <div id="portfolio">
    <!-- Start Portfolio 
    ============================================= -->
    <div id="portfolio" class="portfolio-style-six-area default-padding-top">
      <div class="shape-animated-right">
        <img src="../assets/img/shape/1.webp" alt="Shape" />
      </div>

      <div class="container">
        <div class="heading-left">
          <div class="row align-center">
            <div class="col-lg-5">
              <div class="left-info">
                <h5 class="sub-title">Recent Work</h5>
                <h2 class="title">Look at my portfolio</h2>
                <div class="heading-shape">
                  <img src="../assets/img/shape/10.png" alt="Shape" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="container">
        <div class="row">
          <div class="col-md-12 gallery-content mb--15">
            <div class="magnific-mix-gallery masonary">
              <div id="portfolio-grid" class="gallery-items colums-3">
                <!-- Single Item -->
                <SingleItem v-for="proba in paginatedItems" :item="proba" />
                <!-- End Single Item -->
              </div>
            </div>
          </div>
        </div>
        <div class="pagination">
        <button @click="previousPage" :disabled="currentPage === 1" class="btn-class">Previous</button>
        <button @click="nextPage" :disabled="currentPage === totalPages" class="btn-class">Next</button>
      </div>
      </div>
      

      <!-- Start Projects Single Modal -->
      <SingleModal v-for="modal in respModal" :modal="modal" />
      <!-- End Projects Single Modal -->
    </div>
    <!-- End Portfolio -->
  </div>
</template>

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
