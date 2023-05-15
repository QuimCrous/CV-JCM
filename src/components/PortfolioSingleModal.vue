<template>
  <div>
    <!-- Start Projects Single Modal -->
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

            <div class="project-details-items">
              <div class="project-thumb">
                <img :src="modal.bigImgSrc" alt="Thumb" />
              </div>
              <div class="top-info">
                <div class="row">
                  <div class="col-xl-12 left-info">
                    <div class="project-info mt-md-50 mt-xs-40 mb-40">
                      <div class="content">
                        <ul class="project-basic-info">
                          <!-- <li>Client <span>validthemes</span></li> -->
                          <li>
                            Project Type <span>{{ modal.projectType }}</span>
                          </li>
                          <li>
                            Date <span>{{ modal.date }}</span>
                          </li>
                          <li>
                            Link
                            <span
                              ><a :href="modal.url" target="_blank">{{
                                modal.link
                              }}</a></span
                            >
                          </li>
                        </ul>
                      </div>
                    </div>
                    <h2>{{ modal.title }}</h2>
                    <p
                      class="paragraph-text"
                      v-for="paragraph in modal.description"
                    >
                      {{ paragraph }}
                    </p>
                    <ul class="check-list mt-40">
                      <li>
                        <h4>{{ modal.checklist.titleOne }}</h4>
                        <p
                          class="paragraph-text"
                          v-for="paragraph in modal.checklist.descriptionOne"
                        >
                          {{ paragraph }}
                        </p>
                      </li>
                      <li>
                        <h4>{{ modal.checklist.titleTwo }}</h4>
                        <p
                          class="paragraph-text"
                          v-for="paragraph in modal.checklist.descriptionTwo"
                        >
                          {{ paragraph }}
                        </p>
                      </li>
                    </ul>
                  </div>
                </div>
              </div>

              <div class="main-content mt-40">
                <p
                  class="paragraph-text"
                  v-for="paragraph in modal.bigDescription"
                >
                  {{ paragraph }}
                </p>
                <div class="row">
                  <div class="col-lg-6 col-md-6">
                    <img :src="modal.smallImgSrcOne" alt="Thumb" />
                  </div>
                  <div class="col-lg-6 col-md-6">
                    <img :src="modal.smallImgSrcTwo" alt="Thumb" />
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- End Projects Single Modal -->
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
