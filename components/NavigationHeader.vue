<template>
  <nav
    id="header"
    class="bg-white dark:bg-gray-900 dark:text-white text-gray-900 px-3 p-2 shadow-md flex justify-between"
  >
    <Logo />
    <div class="flex justify-evenly">
      <Button
        text="About us"
        classes="m-1 outline-none dark:text-white text-gray-900 transition duration-500 transform hover:scale-105 ease-in-out rounded-none"
      />
      <Button
        text="Career with us"
        classes="m-1 outline-none dark:text-white text-gray-900 transition duration-500 transform hover:scale-105 ease-in-out rounded-none"
      />
      <!-- <Button
        text="Reach us"
        classes="m-1 outline-none dark:text-white text-gray-900 transition duration-500 transform hover:scale-105 ease-in-out rounded-none"
      /> -->
      <Button
        text="Reach us"
        classes="m-1 px-4 bg-gray-900 dark:bg-white dark:text-gray-900 text-white outline-none transition duration-500 ease-in-out transform hover:scale-105 rounded-md"
      />
    </div>
  </nav>
</template>
<script>
import Logo from "./Logo";
export default {
  components: {
    Logo,
  },
  data() {
    return {};
  },
};
</script>