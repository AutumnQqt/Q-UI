<template>
  <svg class="g-icon" aria-hidden="true">
    <use :xlink:href="`#${name}`"></use>
  </svg>
</template>
<script>
export default {
  props: ['name']
}
</script>
<style lang="scss" scoped>
.g-icon {
  width: 1em; height: 1em;
  vertical-align: -0.15em;
  fill: currentColor;
  overflow: hidden;
}
</style>