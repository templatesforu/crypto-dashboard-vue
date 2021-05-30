<template>
  <div class="button-container"><button class="thqButton button-button">{{ button }}</button></div>
</template>

<script>
export default {
  name: 'Button',
  props: {
    button: {
      type: String,
      default: 'Button',
    },
  },
}
</script>

<style scoped>
.button-container {
  display: flex;
  position: relative;
  align-items: flex-start;
  flex-direction: column;
  justify-content: flex-start;
}
.button-button {
  color: var(--dl-color-gray-white);
  transition: 0.3s;
  font-family: Roboto;
  border-color: var(--dl-color-primary-primary);
  border-radius: var(--dl-radius-radius-radius8);
  background-color: var(--dl-color-primary-primary);
}
</style>
