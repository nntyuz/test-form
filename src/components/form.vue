<template lang="pug">
.form-component.flex.a-center.j-center.column
  h2 Заполните поля
  .wrapper.flex.column
    .flex.a-center
      button.step-button(@click="() => (step = step - 1)" :disabled="step < 1") Назад
      div.step {{ step + 1 }}
      button.step-button(@click="() => (step = step + 1)" :disabled="step >= 2") Вперед
    input(
      v-for="item in config[step]"
      v-model="item.value"
      :key="item.id"
      :placeholder="item.name"
      :type="item.type")
    .w-100.flex(v-if="step === config.length - 1")
      button.form-button Подтвердить
  </template>

<script>
import formConfig from "../helpers/form";

export default {
  name: "FormComponent",
  data() {
    return {
      step: 0,
      config: null,
    };
  },
  created() {
    this.config = formConfig.map((step) =>
      step.map((formField) => ({ ...formField, value: "" }))
    );
  },
};
</script>

<style lang="scss" scoped>
.form-component {
  padding-top: 120px;
  padding-bottom: 120px;
  h2 {
    position: relative;
    font-size: 30px;
    line-height: 30px;
    text-transform: uppercase;
    color: #01237d;
    &::after {
      position: absolute;
      top: -50px;
      left: 50%;
      content: "";
      height: 30px;
      width: 2px;
      background: #d7dce7;
    }
  }
  .wrapper {
    gap: 20px;
    margin-top: 30px;
    input {
      min-width: 852px;
      height: 48px;
      background: #fff;
      border: 1px solid #ededed;
      border-radius: 30px;
      padding-left: 30px;
      padding-right: 30px;
      font-size: 16px;
      line-height: 21px;
      color: #808695;
      &:hover,
      &:focus {
        outline: none;
      }
    }
  }
  .form-button {
    width: 200px;
    height: 50px;
    background: linear-gradient(
      101.49deg,
      #a5a8f5 17.34%,
      #b8baf5 53.55%,
      #9296f7 86.43%
    );
    color: #2a2d54;
    font-size: 14px;
    line-height: 14px;
    text-transform: uppercase;
    border-radius: 100px;
  }
  .step {
    font-size: 14px;
    line-height: 14px;
    margin: 0 20px;
  }
  .step-button {
    width: 100px;
    height: 40px;
    font-size: 12px;
    line-height: 12px;
    background: #01237d;
    color: #fff;
    border-radius: 100px;
    &:disabled {
      opacity: 0.5;
    }
  }
}
</style>
