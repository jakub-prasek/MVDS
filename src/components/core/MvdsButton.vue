<template>
  <component :is="this.tag">
      <slot/>

      </component>
</template>

<script>
export default {
  name: "mvdsbutton",
  props: {
    tag: {
        type: String,
        default: "button",
      validator: function (value) {
        // The value must match one of these strings
        return ["button", "a"].indexOf(value) !== -1;
      },
    },
  },
};
</script>

<style scoped>
</style>