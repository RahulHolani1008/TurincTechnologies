<template>
  <div>
    <NavigationHeader />
    <Nuxt />
    <NavigationFooter />
  </div>
</template>
<script>
import NavigationHeader from "@/components/NavigationHeader";
import NavigationFooter from "@/components/NavigationFooter";
export default {
  components: {
    NavigationHeader,
    NavigationFooter,
  },
};
</script>