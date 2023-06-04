<template>
  <div
    class="text-center text-h3 text-weight-medium"
    style="margin-bottom: 80px"
  >
    Для любых событий и дорогих вам людей
  </div>
  <div class="flex justify-center">
    <div class="flex q-gutter-md" style="max-width: 1200px">
      <div v-for="card in cards" :key="card.title">
        <q-card style="width: 380px; border-radius: 10px">
          <q-img
            :src="require(`../../public/images/content/${card.img}`)"
            alt=""
          />
          <div class="q-card_content">
            <div class="text-h5 text-bold q-card_content__title">
              {{ card.title }}
            </div>
            <div class="text-body1 text-weight-regular q-card_content__text">
              {{ card.description }}
            </div>

            <div class="text-h5 text-weight-medium q-card_content__price">
              {{ card.price }} ₽/шт.
            </div>
            <q-btn
              class="q-card_content__action text-weight-medium"
              label="Заказать"
              flat
            />
          </div>
        </q-card>
      </div>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from "vue";

const props = defineProps({
  cards: Array,
});
</script>

<style lang="scss" scoped>
.q-card_content {
  padding: 50px 0 44px 50px;
  &__title,
  &__text {
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
</style>
