<template>
  <div class="about-me wrapper">
    <div class="about-me__title">
      <h2>About me</h2>
      <img src="/src/assets/moon.jpg" aria-label="фазы луны" />
    </div>

    <div class="about-me__block about-me__block--me">
      <div class="about-me__text">
        <h3>
          Hi i am <br />
          Maxim
        </h3>
        <img src="/src/assets/signs_negate.png" aria-label="знаки зодиака" height="40" />
        <p>
          First of all, you lose the compilation speed which is one of Vite’s big pros (hell, Vite
          means Fast in French). But you now also severely hinder your development
        </p>
        <AppButton> <span>Read more</span></AppButton>
      </div>
      <img src="/src/assets/man.jpg" aria-label="Maxim" width="450" />
    </div>

    <div class="about-me__block about-me__block--journey">
      <img src="/src/assets/map.png" aria-label="карта" width="570" />

      <div class="about-me__text">
        <span class="about-me__subtitle">About me</span>
        <h3>My astro jorney</h3>
        <p>
          First of all, you lose the compilation speed which is one of Vite’s big pros (hell, Vite
          means Fast in French). But you now also severely hinder your development development
        </p>
        <AppButton> <span>Read more</span></AppButton>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import AppButton from '../elements/AppButton.vue'

export default defineComponent({
  components: { AppButton },
  setup() {
    return {}
  }
})
</script>

<style lang="scss">
.about-me {
  padding-top: 170px;

  &__block {
    display: grid;

    button {
      text-transform: uppercase;
      background-color: transparent;
      border: none;
      color: #fff;
      border-bottom: 1px solid #fff;
      padding: 0;
      padding-bottom: 4px;
    }

    h3 {
      font-size: 60px;
      line-height: 76px;
      text-transform: uppercase;
      font-weight: 300;
      letter-spacing: 5px;
      margin: 0;
      margin-bottom: 8px;
    }

    p {
      margin-bottom: 20px;
      margin-top: 8px;
    }

    &__subtitle {
      display: inline-block;
      vertical-align: baseline;
      text-transform: uppercase;
      margin-bottom: 10px;
    }

    &--me {
      grid-template-columns: repeat(2, 450px);
      grid-gap: 50px;

      padding-left: 170px;
      margin-bottom: 120px;
    }

    &--journey {
      grid-template-columns: repeat(2, 1fr);
      grid-gap: 150px;

      .about-me__text {
        padding-top: 65px;
      }
    }
  }

  &__text {
    padding-top: 90px;
  }

  &__title {
    position: relative;
    width: 604px;
    height: 200px;
    margin: 0 auto;
    margin-bottom: 80px;

    img {
      transform: rotate(180deg);
      position: absolute;
      bottom: 0;
    }

    h2 {
      font-size: 50px;
      text-transform: uppercase;
      font-weight: 300;
      letter-spacing: 4px;
      margin: 0;
      position: absolute;
      z-index: 1;
      left: 50%;
      top: 0;
      transform: translateX(-50%);
    }
  }
}
</style>
