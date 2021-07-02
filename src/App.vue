<template lang="pug">
#app
  .g-page
    h1 Gia-PUI - Kitchen sink

    section
      h2 Buttons
      p gia-pui includes several predefined button styles, each serving its own semantic purpose, with a few extras thrown in for more control.
      .types
        h3 Types
        g-button(
          v-for="i in types"
          :type="i"
          :key="i") type={{i}}
        g-button(disabled) disabled

      .sizes
        h3 Sizes
        g-button(
          v-for="i in sizes"
          :size="i"
          :key="i") size={{i}}

</template>

<script>
import Button from '@/components/Button'

export default {
  components: {
    GButton: Button
  },

  data () {
    return {
      types: ['normal', 'primary', 'success', 'warning', 'error'],
      sizes: ['xs', 'sm', 'md', 'lg', 'xl']
    }
  }
}
</script>

<style lang="stylus" scoped>
.buttons
  // > *:not(:last-child)
  //   margin-right 1em
</style>
