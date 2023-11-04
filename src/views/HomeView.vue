<template>
  <div class="home">
    <AboutMe class="home__section" />
    <SubscribeEl />
  </div>
</template>

<script lang="ts">
import SubscribeEl from '@/components/SubscribeEl.vue'
import AboutMe from '@/sections/AboutMe.vue'
import { defineComponent } from 'vue'

export default defineComponent({
  setup() {
    return {}
  },
  components: { AboutMe, SubscribeEl }
})
</script>

<style lang="scss">
.home {
  &__section {
    margin-bottom: 260px;
  }
}
</style>
