<script>
import appHeader from './components/appHeader.vue';
import appMain from './components/appMain.vue';
export default {
  components: {
    appHeader,
    appMain
  }
}
</script>

<template lang="">
  <div>
    <appHeader/>
    <appMain/>
  </div>
</template>
<style lang="scss">
@use './generals.scss';
</style>