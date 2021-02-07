<template>
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
  <!-- {{-- style blade file --}} -->
  <link
    href="https://fonts.googleapis.com/css?family=Rubik:300,400,500,600%7CIBM+Plex+Sans:300,400,500,600,700"
    rel="stylesheet"
  />

  <!-- BEGIN: Vendor CSS-->
  <link rel="stylesheet" type="text/css" href="vendors/vendors.min.css" />
  <!-- @yield('vendor-styles') -->
  <!-- END: Vendor CSS-->

  <!-- BEGIN: Theme CSS-->
  <link rel="stylesheet" type="text/css" href="css/bootstrap.css" />
  <link rel="stylesheet" type="text/css" href="css/bootstrap-extended.css" />
  <link rel="stylesheet" type="text/css" href="css/colors.css" />
  <link rel="stylesheet" type="text/css" href="css/components.css" />
  <link rel="stylesheet" type="text/css" href="css/themes/dark-layout.css" />
  <link rel="stylesheet" type="text/css" href="css/themes/semi-dark-layout.css" />
  <!-- END: Theme CSS-->

  <!-- BEGIN: Page CSS-->
  <link
    v-if="configData.mainLayoutType == 'horizontal-menu'"
    rel="stylesheet"
    type="text/css"
    href="css/core/menu/menu-types/horizontal-menu.css"
  />
  <link v-else rel="stylesheet" type="text/css" href="css/core/menu/menu-types/vertical-menu.css" />
  <!-- @yield('page-styles') -->
  <!-- END: Page CSS-->

  <!-- BEGIN: Custom CSS-->

  <!-- END: Custom CSS-->
    </head>
    <!-- END: Head-->
</template>

<script>
export default {
  name: 'Styles',
};
</script>
