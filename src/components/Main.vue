<template>
  <div class="main">
    <div class="main__wrapper">
      <Menu class="main__menu"></Menu>
      <Form></Form>
    </div>
  </div>
</template>

<script>
import Menu from "./Menu";
import Form from "./Form";
export default {
  name: "Main",
  components: { Menu, Form }
};
</script>

<style lang="scss" scoped>
.main {
  background-color: #000000;
  padding-left: 125px;
  padding-right: 115px;
  &__wrapper {
    display: grid;
    grid-template-columns: 6fr 12fr;
  }
  &__menu {
    height: max-content;
  }
}
</style>



