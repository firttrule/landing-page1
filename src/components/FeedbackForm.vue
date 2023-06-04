<template>
  <div style="background: #081130">
    <div
      style="
        max-width: 1180px;
        padding: 70px 0;
        border-radius: 8px;
        margin: 0 auto 80px;
        background: #ffffff;
      "
    >
      <div class="text-center" style="margin-bottom: 36px">
        <div class="text-h4 text-bold q-mb-sm">
          Чтобы сделать заказ, укажите ваш телефон
        </div>
        <div class="text-h6 text-weight-regular">
          Мы перезвоним в течении 15 минут, чтобы уточнить ваши пожелания
        </div>
      </div>

      <q-form @submit="onSubmit" class="text-center">
        <div
          class="flex justify-center q-gutter-x-md q-mb-md"
          style="height: 80px"
        >
          <input
            placeholder="Номер телефона"
            v-model="phone"
            class="text-weight-regular text-h6"
            type="tel"
            style="
              width: 380px;
              background: #f2f6fa;
              border-radius: 8px;
              border: none;
              padding-left: 44px;
            "
          />

          <q-btn
            class="text-weight-medium text-h6"
            type="submit"
            flat
            style="
              width: 380px;
              background: #fed84c;
              border-radius: 8px;
              color: #2e363e;
            "
          >
            Сделать заказ
          </q-btn>
        </div>

        <div>
          <input
            type="checkbox"
            v-model="accept"
            id="accept"
            style="margin-right: 7px"
          />
          <label for="accept" style="color: #7e868e"
            >Нажимая на кнопку, вы соглашаетесь с
            <a href="#" style="color: #7e868e"
              >условиями обработки персональных данных</a
            >
          </label>
        </div>
      </q-form>
    </div>

    <Footer />
  </div>
</template>

<script setup>
import Footer from "src/components/Footer.vue";
import { useQuasar } from "quasar";
import { ref } from "vue";
import { matPhone } from "@quasar/extras/material-icons";

const $q = useQuasar();
const phone = ref(null);
const accept = ref(false);

const onSubmit = () => {
  if (phone.value == null) {
    $q.notify({
      color: "red-5",
      textColor: "white",
      message: "Введите номер телефона",
    });
  } else if (accept.value !== true) {
    $q.notify({
      color: "red-5",
      textColor: "white",
      message: "Примите условия обработки персональных данных",
    });
  } else {
    $q.notify({
      color: "green-4",
      textColor: "white",
      message: "Заявка отправлена",
    });
    onReset();
  }
};

const onReset = () => {
  phone.value = null;
  accept.value = false;
};
</script>

<style lang="scss" scoped></style>
