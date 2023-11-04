<template>
  <div class="subscribe-el">
    <div class="wrapper">
      <h2>Lunar</h2>
      <div>
        <div>
          <input type="text" placeholder="Name" />
          <input type="email" placeholder="Email" />
          <input type="text" placeholder="Sun sign" />
          <AppButton><span>Subscribe</span></AppButton>
        </div>
        <p>Get your Daily horoscope</p>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import AppButton from '@/elements/AppButton.vue'
import { defineComponent } from 'vue'
export default defineComponent({
  setup() {
    return {}
  },
  components: { AppButton }
})
</script>

<style lang="scss">
.subscribe-el {
  background-image: url('src/assets/lunar.png');
  background-repeat: no-repeat;
  background-position: 0 0;
  background-size: cover;
  color: rgba(#fff, 0.7);
  display: flex;
  flex-direction: column;
  min-height: 149px;
  padding-bottom: 60px;

  h2 {
    font-size: 60px;
    line-height: 70px;
    font-weight: 300;
    text-transform: uppercase;
    letter-spacing: 12px;
    color: #fff;
    text-align: center;
    margin: 0;
    margin-bottom: 20px;
  }

  input {
    min-width: 200px;
    border: none;
    border-bottom: 1px solid rgba(#fff, 0.7);
    background-color: transparent;
    display: inline-block;
    margin-right: 70px;
    transition: all 0.2s;

    &::placeholder {
      text-transform: uppercase;
      color: rgba(#fff, 0.7);
    }

    &:focus {
      color: #fff;
      outline: none;
      border-bottom: 2px solid #fff;

      &::placeholder {
        color: rgba(#fff, 0.9);
      }
    }
  }

  p {
    margin: 0;
    font-size: 14px;
  }

  button {
    color: rgba(#fff, 0.7);
    background-color: transparent;
    border: none;
    text-transform: uppercase;
  }
}
</style>
