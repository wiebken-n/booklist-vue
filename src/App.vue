<template>
  <LayoutHeader />
  <main>
    <BookList />
    <!-- <BaseButton /> -->
  </main>
</template>

<script>
import LayoutHeader from "./components/LayoutHeader.vue";
import BookList from "./components/BookList.vue";
// import BaseButton from "./components/BaseButton.vue";

export default {
  name: "App",
  components: {
    LayoutHeader,
    BookList,
    // BaseButton,
  },
};
</script>

<style>
@import url("./assets/reset.css");
@import url("./assets/global.css");
</style>
