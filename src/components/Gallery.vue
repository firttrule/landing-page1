<template>
  <div class="flex justify-center">
    <div v-for="item in images" :key="item.index">
      <div style="width: 600px; margin: 5px 5px">
        <q-img
          :src="require(`../../public/images/gallery/${item.img}`)"
          alt=""
        />
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
