<template>
  <q-card style="width: 380px">
    <q-img src="../../public/images/content/img.svg" alt="" />
    <div class="q-card_content">
      <div class="text-h5 text-bold q-card_content__title">Кремовый замок</div>
      <div
        class="text-body1 text-weight-regular q-card_content__text"
        style="width: 240px"
      >
        Нежный крем любого цвета на выбор, вафельная основа
      </div>

      <div class="text-h5 text-weight-medium q-card_content__price">
        150 ₽/шт.
      </div>
      <q-btn
        class="q-card_content__action text-weight-medium"
        label="Заказать"
      />
    </div>
  </q-card>
</template>

<script setup>
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
