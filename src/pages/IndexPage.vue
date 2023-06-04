<template>
  <q-page>
    <Catalog :cards="cards" />
    <Gallery :images="images" />
    <FeedbackForm />
  </q-page>
</template>

<script setup>
import { ref } from "vue";
import Catalog from "src/components/Catalog.vue";
import Gallery from "src/components/Gallery.vue";
import FeedbackForm from "src/components/FeedbackForm.vue";

const cards = [
  {
    img: "img.svg",
    title: "Кремовый замок",
    description: "Нежный крем любого цвета на выбор, вафельная основа",
    price: 150,
  },
  {
    img: "img (1).svg",
    title: "Малиновый рай",
    description: "Воздушный крем, темная основа и ягода малины",
    price: 150,
  },
  {
    img: "img (2).svg",
    title: "Фейерверк",
    description: "Разноцветные крем, с бисквитной основой",
    price: 150,
  },
  {
    img: "img (3).svg",
    title: "Шоколадный мир",
    description: "Ореховая стружка, нежный крем и шоколадная основа",
    price: 150,
  },
  {
    img: "img (4).svg",
    title: "Слезы дракона",
    description: "Нежный крем любого цвета на выбор, вафельная основа",
    price: 150,
  },
  {
    img: "img (5).svg",
    title: "Летняя фантазия",
    description: "Украшения в форме сердец, для любимого человека",
    price: 150,
  },
  {
    img: "img (6).svg",
    title: "Мыс безумия",
    description: "Разноцветная основа, стружка и нежный крем",
    price: 150,
  },
  {
    img: "img (7).svg",
    title: "Облачная сказка",
    description: "Светлая основа, нежный крем со стружкой сверху",
    price: 150,
  },
  {
    img: "img (8).svg",
    title: "Темный рыцарь",
    description: "Тёмная основа, нежный крем и вкусные шарики",
    price: 150,
  },
];

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
  font-family: 'Montserrat';
}
</style>
