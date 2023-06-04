<template>
  <q-card
    style="width: 380px; margin: 10px 10px"
    v-for="card in cards"
    :key="card.title"
  >
    <q-img :src="require(`../../public/images/content/${card.img}`)" alt="" />
    <div class="q-card_content">
      <div class="text-h5 text-bold q-card_content__title">
        {{ card.title }}
      </div>
      <div
        class="text-body1 text-weight-regular q-card_content__text"
        style="width: 240px"
      >
        {{ card.description }}
      </div>

      <div class="text-h5 text-weight-medium q-card_content__price">
        {{ card.price }} ₽/шт.
      </div>
      <q-btn
        class="q-card_content__action text-weight-medium"
        label="Заказать"
      />
    </div>
  </q-card>
</template>

<script setup>
import { defineProps } from "vue";

const props = defineProps({
  cards: Array,
});
</script>

<style lang="scss" scoped>
* {
  margin: 0;
  padding: 0;
}

.q-card_content {
  padding: 50px 0 44px 50px;
  &__title,
  &__text {
    font-family: "Montserrat";
    color: #2e363e;
  }
  &__title {
    margin-bottom: 12px;
  }
  &__price {
    margin-top: 24px;
    margin-bottom: 14px;
  }
  &__action {
    background: #fed84c;
    color: #2e363e;
    padding: 20px 40px;
    font-size: 18px;
    border-radius: 8px;
  }
}
</style>>
