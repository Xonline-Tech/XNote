<template>
  <v-navigation-drawer class="bg-grey-lighten-2">

    <full-drawer />
  </v-navigation-drawer>

</template>

<script>
import FullDrawer from "../components/main/fullDrawer/index.vue";

export default {
    name: "main",
  components: {FullDrawer}
}
</script>

<style scoped>

</style>