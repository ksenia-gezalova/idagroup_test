<template>
  <div class="menu">
    <nav class="menu__nav">
      <ul class="menu__list">
        <li
          class="menu__item"
          :class="{'menu__item--active': item.isActive }"
          :key="index"
          v-for="(item, index) in items"
        >{{ item.name }}</li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: "Menu",
  data() {
    return {
      items: [
        {
          name: "Личный кабинет",
          isActive: false
        },
        {
          name: "Платежи",
          isActive: true
        },
        {
          name: "История платежей",
          isActive: false
        },
        {
          name: "Настройки",
          isActive: false
        },
        {
          name: "Выйти",
          isActive: false
        }
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.menu {
  background-color: #1f2229;

  &__item {
    color: #ffffff;
    padding: 25px 0 25px 30px;
    cursor: pointer;
    transition: all 0.3s;
    font-weight: bold;
    font-size: 18px;
    line-height: 25px;

    &:hover,
    &--active {
      color: #999999;
      background-color: #2a2d37;
    }
  }
}
</style>
