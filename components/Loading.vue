<template>
  <lottie
    :width="1024"
    :height="1024"
    :options="lottieOptions"
    v-on:animCreated="handleAnimation"
  />
</template>
<script>
import lottie from "vue-lottie/src/lottie.vue";
import * as animationData from "~/assets/loading-animation.json";
export default {
  components: {
    lottie,
  },
  data() {
    return {
      anim: null, // for saving the reference to the animation
      lottieOptions: { animationData: animationData.default },
    };
  },
  methods: {
    handleAnimation: function (anim) {
      this.anim = anim;
    },
  },
};
</script>
