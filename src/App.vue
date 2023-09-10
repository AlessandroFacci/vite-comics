<script>
import AppHeader from "./components/AppHeader.vue";
import AppContent from "./components/AppContent.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  data() {
    return {};
  },
  components: { AppHeader, AppContent, AppFooter },
};
</script>

<template>
  <AppHeader></AppHeader>
  <AppContent></AppContent>
  <AppFooter></AppFooter>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
</style>
