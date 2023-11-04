<template>
  <div>
    <HeaderSection />
    <RouterView />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import HeaderSection from './sections/HeaderSection.vue'

export default defineComponent({
  setup() {
    return {}
  },
  components: { HeaderSection }
})
</script>

<style lang="scss">
@import '@/styles/base.scss';
</style>
