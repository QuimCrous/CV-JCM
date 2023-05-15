<template>
  <div>
    <BlogNav />
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
          <BlogItem v-for="item in response" :item="item" />
          <!-- End Single item -->
        </div>
      </div>

      <!-- Start Blog Single Modal -->
      <!-- End Blog Single Modal -->
      <BlogModal v-for="modal in respModal" :modal="modal" />
    </div>
    <!-- End Blog -->
  </div>
</template>

<script setup>
import BlogNav from "../components/BlogNav.vue";
import BlogItem from "../components/BlogSingleItem.vue";
import BlogModal from "../components/BlogSingleModal.vue";
import BlogJSON from "../assets/json/blog.json";
import BlogModalJSON from "../assets/json/blogmodal.json";

import { ref, onUpdated, watchEffect, reactive } from "vue";
const response = ref(null);
const respModal = ref(null);

response.value = BlogJSON;
respModal.value = BlogModalJSON;
</script>

<style lang="scss" scoped></style>
