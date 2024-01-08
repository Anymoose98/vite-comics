<script>
import appHeader from './components/appHeader.vue';
import appMain from './components/appMain.vue';
import appFooter from './components/appFooter.vue';

export default {
  components: {
    appHeader,
    appMain,
    appFooter,
  }
}
</script>

<template lang="">
  <div>
    <appHeader/>
    <appMain/>
    <appFooter/>

  </div>
</template>
<style lang="scss">
@use './generals.scss';
</style>