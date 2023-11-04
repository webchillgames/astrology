<template>
  <div class="header-section wrapper">
    <div class="header-section__top">
      <img src="/src/assets/logo.png" aria-label="логотип" width="50" />
    </div>
    <div class="header-section__bottom">
      <MainNav :links="navLinks" />
      <SocialLinks />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import MainNav from '../components/MainNav.vue'
import SocialLinks from '@/components/SocialLinks.vue'

const navLinks = [
  { id: 1, title: `Home`, link: `/` },
  { id: 2, title: `About`, link: `/` },
  { id: 3, title: `Services`, link: `/` },
  { id: 4, title: `Contact`, link: `/` }
]
export default defineComponent({
  components: { MainNav, SocialLinks },
  setup() {
    return { navLinks }
  }
})
</script>

<style lang="scss">
.header-section {
  &__top {
    padding: 5px 0;
  }

  &__bottom {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-top: 6px;
    padding-bottom: 12px;
    border-top: 1px solid rgba(#fff, 0.3);
    border-bottom: 1px solid rgba(#fff, 0.3);
  }
}
</style>
