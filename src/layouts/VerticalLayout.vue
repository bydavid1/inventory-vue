<template>
  <!-- BEGIN: Body-->
<body v-bind:class="['vertical-layout', 'vertical-menu-modern', '2-columns',
  configData.isMenuCollapsed == true ? 'menu-collapsed' : '',
  configData.theme + '-layout',
  configData.isContentSidebar === true ? 'content-left-sidebar' : '',
  configData.navbarType,
  configData.footerType,
  configData.bodyCustomClass,
  configData.mainLayoutType === 'vertical-menu-boxicons' ? 'boxicon-layout' : '',
  configData.isCardShadow === false ? 'no-card-shadow' : '']"
  data-open="click" data-menu="vertical-menu-modern" data-col="2-columns">

  <!-- BEGIN: Header-->
  <Navbar/>
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
        <div class="content-overlay"></div>
      <div class="content-wrapper">
        <div class="content-header row">
        </div>
        <div class="content-body">
          <slot name="content"><slot>
        </div>
      </div>
    </div>
  </div>
  <!-- {{-- others page structures --}} -->
  <div v-else>
  <div class="content-overlay"></div>
  <div class="content-wrapper">
      <div class="content-header row" v-if="configData.pageHeader === true">
        <Breadcrumb/>
      </div>
    <div class="content-body">
          <slot name="content"><slot>
    </div>
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
import Navbar from '../components/Navbar.vue';
import Sidebar from '../components/Sidebar.vue';
import Breadcrumb from '../components/Breadcrumbs.vue';
import Customizer from '../components/Customizer.vue';
import Footer from '../components/Footer.vue';
import Scripts from '../components/Scripts.vue';

export default {
  name: 'VerticalLayout',
  components: {
    Navbar,
    Sidebar,
    Breadcrumb,
    Customizer,
    Footer,
    Scripts,
  },
};
</script>
