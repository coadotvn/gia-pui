<template lang="pug">
button.g-button.g-boxed(:class="classes")
  slot
</template>

<script>
export default {
  props: {
    disabled: {
      type: Boolean,
      default: false
    },

    type: {
      type: String,
      default: 'default'
    },

    size: {
      type: String,
      default: 'md'
    }
  },

  computed: {
    classes () {
      return {
        'g-disabled': this.disabled,
        [`g-${this.type}`]: true,
        [`g-${this.size}`]: true
      }
    }
  }
}
</script>
