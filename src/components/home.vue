<template>
  <div class="layout">
    <v-header></v-header>
    <v-content></v-content>
  </div>
</template>

<script>
import vHeader from "./view/header";
import vContent from "./view/content";
export default {
  components: {
    vHeader,
    vContent
  }
};
</script>

<style scoped>

</style>
