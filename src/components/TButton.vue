<template>
  <button @click="onClick">{{ label }}</button>
</template>

<script setup>

// export default {
//   props: {
//     label: String
//   }
// }

const props = defineProps ({
  label: String
})

console.log(props.label)

const onClick = () => {
  console.log('i have been clicked')
}

</script>

<style scoped lang="stylus">
@import '../styles/variables.styl'

button
  background: $primary-color
  padding: .35em .7em
  font-size: 1.2rem
  border: 1px solid $border-color
  border-radius: 5px
  if light($primary-color)
    color: $dark-text-color
  else
    color: $light-text-color
  cursor: pointer
  transition: background-color .4s ease
  &:hover
    if light($primary-color)
      background: lighten($primary-color, 30%)
    else
      background: darken($primary-color, 30%)
</style>