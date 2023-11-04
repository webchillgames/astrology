<template>
  <nav class="main-nav">
    <ul>
      <li v-for="l in links" :key="l.id">
        <a :href="l.link">
          <span>{{ l.title }}</span>
        </a>
      </li>
    </ul>
  </nav>
</template>

<script lang="ts">
import { defineComponent, type PropType } from 'vue'
import type { navLink } from '@/types'

export default defineComponent({
  props: {
    links: Array as PropType<navLink[]>
  },
  setup() {
    return {}
  }
})
</script>

<style lang="scss">
.main-nav {
  ul {
    @include resetListStyles;
    display: flex;
  }

  a {
    color: #fff;
    text-decoration: none;
    padding: 0 32px;
    text-transform: uppercase;
    font-size: 10px;
    letter-spacing: 4px;
  }

  li {
    &:first-child a {
      padding-left: 0;
    }
  }
}
</style>
