<template>
  <img class="emblem" :src="src" alt="Eric Davis - Fullstack Developer" />
</template>

<script>
export default {
  name: 'HeaderEmblem',
  props: {
    theme: String
  },
  computed: {
    src() {
      switch (this.theme) {
        case 'theme-80s':
          return '/img/emblem-80s.png';
        default:
          return '/img/emblem-90s.png';
      }
    }
  }
}
</script>

<style scoped>
.theme-90s .emblem {
  max-width: 90px;
}
</style>

