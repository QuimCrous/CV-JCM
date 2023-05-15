<template>
  <div>
    <!-- Single Item -->
    <div class="pf-item">
      <div class="overlay-content">
        <img :src="item.imageSrc" alt="thumb" />
        <div class="content">
          <div class="title">
            <span>{{ item.title }}</span>
            <h5>
              <a
                href="#"
                data-bs-toggle="modal"
                :data-bs-target="item.dataBsTarget"
                >{{ item.description }}</a
              >
            </h5>
          </div>
          <a
            href="#"
            data-bs-toggle="modal"
            data-bs-target="#projectSingleModal"
            ><i class="fas fa-arrow-right"></i
          ></a>
        </div>
      </div>
    </div>
    <!-- End Single Item -->
  </div>
</template>

<script setup>
import { ref, onUpdated, watchEffect, reactive } from "vue";
const props = defineProps({
  item: Object,
});
</script>

<style lang="scss" scoped></style>
