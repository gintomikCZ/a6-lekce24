<template>

  <TButton :label="buttonLabel"/>
  <div>{{ anotherValue }}</div>
  <div>{{ fullName }}</div>

</template>

<script setup>

import TButton from '@/components/TButton.vue'
// export default {
//   name: 'App',
//   data() {
//     return {
//       buttonLabel: 'click me!'
//     }
//   },
//   components: { TButton }
// }

import { ref, computed } from 'vue'

const buttonLabel = ref('click me!')
const anotherValue = ref('lalala')
anotherValue.value = 'ahoj'
const firstname = ref('Karel')
const lastname = ref('Houska')

const fullName = computed(() => firstname.value + ' ' + lastname.value)




</script>