<template>
<html class="loading" lang="es">

    <Styles/>

    <VerticalLayout v-if="configData.mainLayoutType == 'vertical-menu'"/>
    <HorizontalLayout v-else/>
     <!-- {{-- if mainLaoutType is empty or not set then its print below line --}} -->
     <!-- <h1>{{alert('mainLayoutType Option is empty in config custom.php file.')}}</h1> -->

</html>
</template>

<script>
import Styles from '../components/Styles.vue';
import HorizontalLayout from '../layouts/HorizontalLayout.vue';
import VerticalLayout from '../layouts/VerticalLayout.vue';

export default {
  name: 'System',
  components: {
    Styles,
    HorizontalLayout,
    VerticalLayout,
  },
  computed: {
    configData() { return this.$store.state.configData; },
  },
};
</script>
