<template>
  <div>
    <!-- Start Blog Single Modal -->
    <div
      class="modal fade"
      :id="modal.modalId"
      tabindex="-1"
      aria-hidden="true"
    >
      <div
        class="modal-dialog modal-dialog-centered modal-dialog-scrollable modal-xl"
      >
        <div class="modal-content">
          <div class="modal-body">
            <div class="modal-header">
              <button
                type="button"
                class="btn-close"
                data-bs-dismiss="modal"
                aria-label="Close"
              ></button>
            </div>

            <div class="blog-single-content">
              <div class="thumb">
                <a href="#"><img :src="modal.srcImgOne" alt="Thumb" /></a>
              </div>
              <div class="info">
                <p class="paragraph-text">
                  {{ modal.pOne }}
                </p>
                <p class="paragraph-text">
                  {{ modal.pTwo }}
                </p>
                <p class="paragraph-text">
                  {{ modal.pThree }}
                </p>
                <blockquote>
                  {{ modal.blockquote }}
                </blockquote>
              </div>
            </div>

            <!-- Post Author -->
            <div class="post-author">
              <div class="thumb">
                <img :src="modal.profileImg" alt="Thumb" />
              </div>
              <div class="content">
                <h4>
                  <a href="#">{{ modal.profileName }}</a>
                </h4>
                <p>
                  {{ modal.profileInfo }}
                </p>
              </div>
            </div>
            <!-- Post Author -->

            <!-- Post Tags Share -->
            <div class="post-tags share">
              <div class="tags">
                <h4>Tags:</h4>
                <a href="#">Algorithm</a>
                <a href="$">Data science</a>
                <a :href="`#${tag}`" v-for="tag in modal.tags">{{ tag }}</a>
              </div>
            </div>
            <!-- Post Tags Share -->
          </div>
        </div>
      </div>
    </div>
    <!-- End Blog Single Modal -->
  </div>
</template>

<script setup>
import { ref, onUpdated, watchEffect, reactive } from "vue";
const props = defineProps({
  modal: Object,
});
</script>

<style scoped>
.paragraph-text {
  text-indent: 30px;
  text-align: justify;
}
</style>
