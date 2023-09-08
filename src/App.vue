<script>
import appHeader from "./components/appHeader.vue";
import appMain from "./components/appMain.vue";
import appFooter from "./components/appFooter.vue";
import appFooterLinks from "./components/appFooterLinks.vue";
import appFooterSocial from "./components/appFooterSocial.vue";

export default {
  components: {
    appHeader,
    appMain,
    appFooter,
    appFooterLinks,
    appFooterSocial,
  },
};
</script>

<template>
  <appHeader />
  <appMain />
  <appFooter />
  <appFooterLinks />
  <appFooterSocial />
</template>

<style lang="scss">
@use "./components/general.scss" as *;
</style>
