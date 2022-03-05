<template>
  <img class="logo" :src="src" alt="Eric Davis - Fullstack Developer" />
</template>

<script>
export default {
  name: 'MainLogo',
  props: {
    theme: String
  },
  computed: {
    src() {
      switch (this.theme) {
        case 'theme-80s':
          return '/img/logo-80s.png';
        default:
          return '/img/logo-90s.png';
      }
    }
  }
}
</script>

<style scoped>
.logo {
  margin: 0 auto;
  display: block;
}

.theme-90s .logo {
  max-width: 700px;
}
</style>

