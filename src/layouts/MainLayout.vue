<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated reveal bordered>
      <div class="flex justify-around items-center q-py-md">
        <div class="text-center text-weight-medium text-h5">Сладкий сундук</div>

        <div class="flex items-center q-gutter-xl">
          <div class="text-weight-regular">
            г. Санкт Петербург, <br />
            ул. Куйбышева 31
          </div>
          <div class="">
            <div class="text-bold text-h6">8 (812) 844-95-49</div>
            <div class="text-weight-regular">Ежедневно с 9:00 до 20:00</div>
          </div>
        </div>
      </div>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { ref } from "vue";
</script>
