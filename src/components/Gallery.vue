<template>
  <div class="text-center" style="margin-bottom: 80px">
    <div class="text-h3 text-weight-medium" style="margin-bottom: 14px">
      Сделали более 3.000 заказов за 2 года
    </div>
    <div class="text-h5">
      Посмотрите фото реальных заказов из нашего instagram
    </div>
  </div>
  <div class="flex justify-center q-gutter-sm">
    <div v-for="item in images" :key="item.index">
      <div style="width: 600px">
        <q-img :src="require(`/public/images/gallery/${item.img}`)" alt="" />
      </div>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from "vue";

const props = defineProps({
  images: Array,
});
</script>

<style lang="scss" scoped></style>
