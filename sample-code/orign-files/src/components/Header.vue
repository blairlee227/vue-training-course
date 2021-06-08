<template>
  <div id="header">
    <h1>{{ pageTitle }}</h1>
  </div>
</template>
<script>
export default {
  name: "Header",
  props: {
    pageTitle: {
      type: String,
      default: "",
    },
  },
};
</script>
<style lang="scss">
@import "@/assets/css/colors";
#header {
  background-color: white;
  height: 150px;
  padding: 30px 200px;
  h1 {
    font-size: 50px;
    color: $primary;
    font-weight: 900;
  }
}
</style>
