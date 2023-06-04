<template>
  <div
    v-for="item in images"
    :key="item.index"
    class="flex"
    style="width: 100%"
  >
    <q-img
      style="width: calc(100% / 3)"
      :src="require(`../../public/images/gallery/${item.img}`)"
      alt=""
    />
  </div>
</template>

<script setup>
const images = [
  {
    img: "photo.svg",
  },
  {
    img: "photo (1).svg",
  },
  {
    img: "photo (2).svg",
  },
  {
    img: "photo (3).svg",
  },
  {
    img: "photo (4).svg",
  },
  {
    img: "photo (5).svg",
  },
  {
    img: "photo (6).svg",
  },
  {
    img: "photo (7).svg",
  },
  {
    img: "photo (8).svg",
  },
];
</script>

<style lang="scss" scoped>
* {
  margin: 0;
  padding: 0;
}
</style>
