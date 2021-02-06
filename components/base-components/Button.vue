<template>
  <button
    :class="classes"
    class="p-2 select-none"
    @click.prevent="$emit('click')"
  >
    {{ text }}
  </button>
</template>
<script>
export default {
  props: {
    text: {
      type: String,
      required: true,
    },
    classes: {
      type: String,
      default: "",
    },
  },
};
</script>