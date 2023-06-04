<template>
  <router-view />
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "App",
});
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;700&display=swap");

* {
  margin: 0;
  padding: 0;
  font-family: "Montserrat";
}
</style>
