<template>
  <footer v-bind:class="['footer', 'footer-light', configData.footerClass]">
    <p class="clearfix mb-0">
      <span class="float-left d-inline-block">2020 &copy; PIXINVENT</span>
      <span class="float-right d-sm-inline-block d-none"
        >Crafted with <i class="bx bxs-heart pink mx-50 font-small-3"></i>by
        <a class="text-uppercase" href="https://1.envato.market/pixinvent_portfolio" target="_blank"
          >Pixinvent</a
        >
      </span>
      <button
        class="btn btn-primary btn-icon scroll-top"
        type="button"
        v-if="configData.isScrollTop"
      >
        <i class="bx bx-up-arrow-alt"></i>
      </button>
    </p>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  computed: {
    configData() { return this.$store.state.configData; },
  },
};
</script>
