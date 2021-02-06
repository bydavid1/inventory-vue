<template>
  <!-- BEGIN: Vendor JS-->
  <script src="vendors/vendors.min.js"></script>
  <script src="assets/fonts/LivIconsEvo/js/LivIconsEvo.tools.js"></script>
  <script src="assets/fonts/LivIconsEvo/js/LivIconsEvo.defaults.js"></script>
  <script src="assets/fonts/LivIconsEvo/js/LivIconsEvo.min.js"></script>
  <!-- BEGIN Vendor JS-->

  <!-- BEGIN: Page Vendor JS-->

  <!-- END: Page Vendor JS-->

  <!-- BEGIN: Theme JS-->
  <script
    v-if="configData.mainLayoutType == 'vertical-menu'"
    src="js/scripts/configs/vertical-menu-light.js"
  ></script>
  <script v-else src="js/scripts/configs/horizontal-menu.js"></script>
  <script src="js/core/app-menu.js"></script>
  <script src="js/core/app.js"></script>
  <script src="js/scripts/components.js"></script>
  <script src="js/scripts/footer.js"></script>
  <script src="js/scripts/customizer.js"></script>

  <!-- END: Theme JS-->

  <!-- BEGIN: Page JS-->
</template>

<script>
export default {
  name: 'Scripts',
  computed: {
    configData() { return this.$store.state.configData; },
  },
};
</script>
