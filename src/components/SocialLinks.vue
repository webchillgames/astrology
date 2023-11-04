<template>
  <div class="social-links">
    <a href="/" aria-label="facebook" class="social-links__icon--facebook social-links__icon"> </a>
    <a href="/" aria-label="twitter" class="social-links__icon--twitter social-links__icon"> </a>
    <a href="/" aria-label="instagram" class="social-links__icon--instagram social-links__icon">
    </a>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
export default defineComponent({
  setup() {
    return {}
  }
})
</script>

<style lang="scss">
.social-links {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 20px;

  &__icon {
    display: block;
    height: 21px;
    background-image: url('src/assets/socials.svg');
    background-repeat: no-repeat;

    &--facebook {
      background-position: 0 -42px;
      width: 22px;
    }

    &--twitter {
      background-position: 0 0;
      width: 28px;
    }

    &--instagram {
      background-position: 0px -20px;
      width: 22px;
    }
  }
}
</style>
