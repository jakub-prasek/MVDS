<template>
  <showcase-colors/>
  <showcase-space/>
  <showcase-buttons/>

</template>

<script>
import ShowcaseButtons from './components/ShowcaseButtons.vue';
import ShowcaseColors from './components/ShowcaseColors.vue';
import ShowcaseSpace from './components/ShowcaseSpace.vue';

export default {
  name: 'App',
  components: {
    ShowcaseColors,
    ShowcaseSpace,
    ShowcaseButtons,
  }
}
</script>

,
    MvdsButton<style>
@import url(./styles/variables.css);
@import url(./styles/typography.css);
</style>
