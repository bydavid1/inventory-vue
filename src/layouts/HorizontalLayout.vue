<template>
  <body v-bind:class="['horizontal-layout', 'horizontal-menu',
    configData.navbarType != 'navbar-hidden' ? configData.navbarType : 'navbar-sticky',
    configData.theme + '-layout',
    configData.isContentSidebar == true ? 'content-left-sidebar' : '',
    configData.footerType,
    configData.bodyCustomClass,
    configData.isCardShadow === false ? 'isCardShadow' : '',
    '2-columns'
    ]" data-open="hover" data-menu="horizontal-menu" data-col="2-columns">

    <!-- BEGIN: Header-->
    <HorizontalNavbar/>
    <!-- END: Header-->

    <!-- BEGIN: Main Menu-->
    <Sidebar/>
    <!-- END: Main Menu-->

    <!-- BEGIN: Content-->
    <div class="app-content content">
      <!-- {{-- Application page structure --}} -->
      <div class="content-area-wrapper" v-if="configData.isContentSidebar === true">
          <div class="sidebar-left">
              <div class="sidebar">
                <slot name="sidebar-content"></slot>
              </div>
          </div>
          <div class="content-right">
              <div class="content-wrapper">
                  <div class="content-header row">
                  </div>
                  <div class="content-body">
                    Footer<slot name="content"><slot>
                  </div>
              </div>
          </div>
      </div>
      <!-- {{-- if full width is required--}} -->
      <div v-bind:class="[configData.extendApp == true ? 'px-0' : 'content-wrapper ']">
        <div class="content-header row" v-if="configData.pageHeader === true">
          <Breadcrumb/>
        </div>

        <div class="content-body">
          <slot name="content"><slot>
        </div>
      </div>
    </div>
    <!-- END: Content-->
    <!-- BEGIN: Customizer-->
    <div class="customizer d-none d-md-block" v-if="configData.isCustomizer === true">
        <a class="customizer-close" href="#"><i class="bx bx-x"></i></a>
        <a class="customizer-toggle" href="#"><i class="bx bx-cog bx bx-spin white"></i></a>
        <Customizer/>
    </div>
    <!-- End: Customizer-->

    <div class="sidenav-overlay"></div>
    <div class="drag-target"></div>

    <!-- BEGIN: Footer-->
    <Footer/>
    <!-- END: Footer-->

    <Scripts/>
  </body>
  <!-- END: Body-->
</template>

<script>
import HorizontalNavbar from '../components/HorizontalNavbar.vue';
import Sidebar from '../components/Sidebar.vue';
import Breadcrumb from '../components/Breadcrumbs.vue';
import Customizer from '../components/Customizer.vue';
import Footer from '../components/Footer.vue';
import Scripts from '../components/Scripts.vue';

export default {
  name: 'HorizontalLayout',
  props: {
    configData: {
      type: Object,
      required: true,
    },
  },
  components: [
    HorizontalNavbar,
    Sidebar,
    Breadcrumb,
    Footer,
    Customizer,
    Scripts,
  ],
};
</script>
