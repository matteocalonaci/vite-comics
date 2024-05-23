<!-- JS -->
<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

export default {
    components: {
      AppHeader,
      AppMain,
      AppFooter
    },

    data() {
        return {

        }
    }
}
</script>

<!-- HTML -->
<template>
  <AppHeader />
  <AppMain/>
  <AppFooter />
</template>


<!-- CSS -->
<style></style>