<template>
  <div>
    <div class="form">
      <p class="form__text">Информация по оплате:</p>
      <div class="form__wrapper">
        <label for="number" class="form__label">Номер счета:</label>
        <input id="number" type="text" class="form__input" v-model="number">
      </div>
      <div class="form__wrapper">
        <label for="amount" class="form__label">Сумма платежа:</label>
        <input
          id="amount"
          type="text"
          class="form__input"
          v-model="amount"
          @change="amount+=' руб'"
        >
      </div>
      <h4 class="form__title">Данные банковской карты</h4>
      <div class="form__holder">
        <div class="form__card form__card--front">
          <p class="form__card-text">Номер карты</p>
          <div class="form__card-wrapper">
            <input type="text" class="form__card-number">
            <input type="text" class="form__card-number">
            <input type="text" class="form__card-number">
            <input type="text" class="form__card-number">
          </div>
          <p class="form__card-text form__card-text--duration">Срок действия</p>
          <div class="form__card-wrapper">
            <input type="text" class="form__card-duration">
            <input type="text" class="form__card-duration form__card-duration--year">
          </div>
          <input type="text" class="form__card-holder" placeholder="Держатель карты">
        </div>
        <div class="form__card form__card--back">
          <div class="form__card-line"></div>
          <p class="form__card-text form__card-text--code">Код CVV2 / CVC2</p>
          <div class="form__card-icon">
            <input type="text" class="form__card-code">
          </div>
        </div>
      </div>
      <button type="button" class="form__button">Оплатить</button>
    </div>
    <div class="form__note">
      <p>Исходя из астатической системы координат Булгакова, соединение стабильно. Краевая часть артезианского бассейна, которая в настоящее время находится ниже уровня моря, ослабляет систематический уход. Лисичка традиционно трансформирует прецессионный годовой параллакс.</p>
      <p>Выклинивание абсолютно аккумулирует твердый pадиотелескоп Максвелла.</p>
      <p>Алмаз слагает горст. Делювий длительно колеблет лазерный подвижный объект.</p>
      <p>Устойчивость, например, параллельна. Аргумент перигелия определяет боксит. Проекция вертикально дает уходящий диабаз. Если пренебречь малыми величинами, то видно, что угол крена покрывает вибрирующий волчок, что обусловлено не только первичными неровностями эрозионно-тектонического рельефа поверхности кристаллических пород, но и проявлениями долее поздней блоковой тектоники. Засветка неба заставляет иначе взглянуть на то, что такое волчок.</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Form",
  data() {
    return {
      number: "87123658716587",
      amount: "100"
    };
  }
};
</script>

<style lang="scss" scoped>
.form {
  font-family: "Arial", Helvetica, sans-serif;
  background-color: #ffffff;
  color: #9fabbc;
  padding: 30px 0 42px 30px;
  font-size: 16px;

  &__text {
    margin-bottom: 20px;
  }

  &__wrapper {
    display: flex;
    align-items: center;
    margin-bottom: 10px;
  }

  &__label {
    margin-right: 40px;
  }

  &__input {
    padding: 1px 0 1px 8px;
    border: none;
    display: block;
    //width: max-content;
  }

  &__title {
    color: #333333;
    font-size: 22px;
    //letter-spacing: 0.5px;
    margin-bottom: 20px;
    font-family: "Open Sans", Helvetica, Arial, sans-serif;
  }

  &__holder {
    display: flex;
  }

  &__card {
    input {
      border: 1px solid #e4e9ee;
      text-align: center;
    }
    padding-left: 15px;
    background-color: #ffffff;
    width: 334px;
    height: 235px;
    border: 1px solid #bebbbb;
    border-radius: 13px;
    position: relative;
    &-text {
      margin-top: 25px;
      margin-bottom: 3px;

      &--duration {
        margin-top: 13px;
      }

      &--code {
        margin-top: 17px;
        margin-right: 23px;
      }
    }

    &-code {
      margin-right: 15px;
      width: 135px;
      height: 40px;
    }

    &-number {
      width: 40px;
      height: 39px;
      margin-right: 10px;
      padding: 0 10px;
    }
    &-duration {
      width: 45px;
      height: 40px;
      margin-right: 10px;
      padding: 0 10px;

      &--year {
        width: 60px;
      }
    }

    &-holder {
      padding: 14px 0 11px 13px;
      margin-top: 11px;
      width: 300px;
      text-align: left !important;
    }
    &-line {
      background-color: #afb3b6;
      height: 40px;
      margin-top: 28px;
    }
    &--front {
      z-index: 10;
    }
    &--back {
      text-align: right;
      margin-top: 20px;
      margin-left: -158px;
      width: 355px;
    }
  }

  &__button {
    font-family: "Open Sans", Helvetica, Arial, sans-serif;
    background-color: #0052ae;
    color: #ffffff;
    font-weight: bold;
    margin-top: 22px;
    padding: 11px 32px;
    margin-left: 14px;
    border: none;
    letter-spacing: 0.5px;
    border-radius: 30px;
    cursor: pointer;
    transition: all 0.4s;

    &:hover {
      opacity: 0.8;
    }
  }
  &__note {
    font-family: "Arial", Helvetica, sans-serif;
    background-color: #333333;
    color: #999999;
    padding-left: 30px;
    //padding-top: 24px;
    padding-bottom: 35px;
    padding-right: 20px;
    font-size: 12px;
    line-height: 20px;
    p {
      margin-top: 0;
      margin-bottom: 0;
      padding-top: 20px;
    }
  }
}
</style>


