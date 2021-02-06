<template>
  <button :class="classes" class="p-2 select-none">{{ text }}</button>
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