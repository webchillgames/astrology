<template>
  <ul>
    <li v-for="c in contacts" :key="c.id">
     <div>
        
     </div>
    </li>
  </ul>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
const contacts = [
  { id: 1, title: '', data: '', icon: '' },
  { id: 2, title: '', data: '', icon: '' }
]
export default defineComponent({
  setup() {
    return { contacts }
  }
})
</script>

<style lang="scss"></style>
