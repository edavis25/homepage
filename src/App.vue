<template>
  <div>
    <theme-provider v-slot="{ theme }">
      <main-header :theme="theme"></main-header>
      <div class="content">
        <logo :theme="theme" />
        <div> HI!</div>
      </div>
    </theme-provider>
  </div>
</template>

<script>
import Logo from '@/components/MainLogo.vue';
import MainHeader from "@/components/MainHeader";
import ThemeProvider from '@/components/providers/ThemeProvider.vue';

export default {
  name: 'App',
  components: {
    Logo,
    MainHeader,
    ThemeProvider
  }
}
</script>

<style>
#app {
  max-width: var(--lg);
  margin: 0 auto;
}
.content {
  display: grid;
  grid-row-gap: var(--space-md);
}
</style>
