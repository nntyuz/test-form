<template lang="pug">
.header-component
  .w-container.flex.a-center.j-between
    .logo.c-white Logo
    .navigation.flex.a-center.j-center
      a(href="#") Главная
      a(href="#") О нас
      a(href="#") Отзывы
      a(href="#") Вопрос-ответ
      a(href="#") Регистрация
      a(href="#") Контакты
    .contacts.flex.column.a-end
      a(href="tel:+7 (800) 555-35-35").tel 8 (800) 555-35-35
      a(href="mailto:test@test.ru").mail test@test.ru
  </template>

<script>
export default {
  name: "HeaderComponent",
};
</script>

<style lang="scss" scoped>
.header-component {
  width: 100%;
  position: absolute;
  top: 0;
  padding-top: 20px;
  z-index: 2;
  .logo {
    font-weight: 700;
    font-size: 40px;
    line-height: 50px;
    text-transform: uppercase;
  }
  .navigation {
    gap: 26px;
    a {
      color: #f1f1f1;
      font-size: 14px;
      line-height: 22px;
      font-weight: 400;
      transition: 300ms ease;
      &:hover {
        color: #a5a8f5;
      }
    }
  }
  .contacts {
    gap: 1px;
    .tel {
      color: #a5a8f5;
      font-size: 14px;
      line-height: 22px;
      transition: 300ms ease;
      &:hover {
        opacity: 0.5;
      }
    }
    .mail {
      font-size: 14px;
      line-height: 22px;
      color: #f1f1f1;
      transition: 300ms ease;
      &:hover {
        color: #a5a8f5;
      }
    }
  }
}
</style>
