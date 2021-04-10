<template>
  <button class='g-button'>
    <g-icon v-if="icon" :name="icon" :class="{[`icon-${iconPosition}`]: true}"></g-icon>
    <slot />
  </button>
</template>

<script>

export default {
  data() {
    return {}
  },
  props: {
    icon: {
      type: String,
      default: ""
    },
    iconPosition: {
      type: String,
      default: 'left',
      validator(value) {
        return !(value !== 'left' && value !== 'right')
      }
    }
  }

}
</script>

<style lang="scss">
.g-button {
  font-size: var(--font-size); height: var(--button-height); padding: 0 1em;
  border-radius: var(--border-radius); border: 1px solid var(--border-color); background: var(--button-bg); 
  display: inline-flex; justify-content: center; align-items: center; vertical-align: middle;
  &:hover { border-color: var(--border-color-hover); }
  &:active { background-color: var(--button-active-color); }
  &:focus { outline: none; }
  .icon { margin-right: .3em; }
  .icon-right { order: 2; margin-right: 0; margin-left: .3em; }
}
</style>
