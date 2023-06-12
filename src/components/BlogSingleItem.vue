<template>
  <div class="blog-style-one mb-30 col-lg-4 col-md-6">
    <div class="item">
      <div class="thumb">
        <a href="#" data-bs-toggle="modal" :data-bs-target="item.dataBsTarget"><img class="object-fill" :src="item.imageSrc" alt="Thumb"/></a>
      </div>
      <div class="info">
        <h4>
          <a
            href="#"
            data-bs-toggle="modal"
            :data-bs-target="item.dataBsTarget"
            >{{ item.title }}</a
          >
        </h4>
        <div class="meta">
          <ul>
            <li>
              <a href="#"><i class="fas fa-user-circle"></i> Quim</a>
            </li>
            <li><i class="fas fa-calendar-alt"></i>{{ item.date }}</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onUpdated, watchEffect, reactive } from "vue";
const props = defineProps({
  item: Object,
});
</script>

<style lang="scss" scoped></style>
