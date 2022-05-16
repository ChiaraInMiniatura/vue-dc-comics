<template>
  <div>
    <HeaderComponent/>
    <MainComponent/>
    <BlueSection/>
    <FooterComponent/>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import BlueSection from './components/BlueSection.vue';

export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent,
    FooterComponent,
    BlueSection
}
}
</script>

<style lang="scss">
@import './assets/style/general';
@import './assets/style/utils';
@import './assets/style/vars';

</style>
