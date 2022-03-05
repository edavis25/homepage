<template>
  <div class="header">
    <div>
      <header-emblem :theme="theme"></header-emblem>
    </div>
    <ul class="header__list">
      <li class="text-xxl">Resume</li>
      <li>Resume</li>
      <li>Resume</li>
      <li>Resume</li>
    </ul>
  </div>
</template>

<script>

import HeaderEmblem from "@/components/HeaderEmblem";
export default {
  name: 'MainHeader',
  components: {HeaderEmblem},
  props: {
    theme: String
  }
}
</script>

<style scoped>
.header {
  position: sticky;
  top: 0;
  font-family: var(--font-section-heading);
  display: flex;
  justify-content: space-between;
  margin-bottom: var(--space-xl);
}
.header__list {
  display: flex;
  list-style-type: none;
  align-items: center;
  gap: var(--space-xl);
}
</style>