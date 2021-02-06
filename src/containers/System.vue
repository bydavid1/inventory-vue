<template>
<html class="loading" lang="es">
  <!-- BEGIN: Head-->

    <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=0">
    <meta name="csrf-token" content="token">

    <title><slot name="pageTitle"></slot></title>
    <!--<link rel="apple-touch-icon" href="{{asset('images/ico/apple-icon-120.png')}}">
    <link rel="shortcut icon" type="image/x-icon" href="{{asset('images/ico/favicon.ico')}}">-->

    <!-- {{-- Include core + vendor Styles --}} -->
    <!-- <Styles/> -->
    </head>
    <!-- END: Head-->
    <VerticalLayout v-if="configData.mainLayoutType == 'vertical-menu'"/>
    <HorizontalLayout v-else/>
     <!-- {{-- if mainLaoutType is empty or not set then its print below line --}} -->
     <h1>{{alert('mainLayoutType Option is empty in config custom.php file.')}}</h1>

</html>
</template>

<script>
import Styles from '../components/Styles.vue';
import HorizontalLayout from '../layouts/HorizontalLayout.vue';
import VerticalLayout from '../layouts/VerticalLayout.vue';

export default {
  name: 'System',
  components: [
    Styles,
    HorizontalLayout,
    VerticalLayout,
  ],
  computed: {
    configData() { return this.$store.state.configData; },
  },
};
</script>
