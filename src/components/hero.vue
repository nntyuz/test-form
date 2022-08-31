<template lang="pug">
.hero-component.flex.a-center.j-center
  img.bg(src="/img/background.png")
  .wrapper.flex-a-center.j-center
    .title
      h1 Lorem Ipsum
      .sub Lorem ipsum is placeholder.
    .search.flex.a-center.j-center
      input(type="text" placeholder="Поиск")
      button.search-button Найти
  </template>

<script>
export default {
  name: "HeroComponent",
};
</script>

<style lang="scss" scoped>
.hero-component {
  .bg {
    position: relative;
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  .wrapper {
    position: absolute;
    .title {
      text-align: center;
      h1 {
        color: #fdfdfd;
        font-size: 40px;
        line-height: 40px;
        text-transform: uppercase;
        opacity: 0.77;
      }
      .sub {
        margin-top: 10px;
        color: #fdfdfd;
        font-size: 14px;
        line-height: 14px;
        opacity: 0.77;
      }
    }
    .search {
      margin-top: 50px;
      position: relative;
      input {
        min-width: 800px;
        height: 48px;
        background: #fff;
        border: 1px solid #f1f1f1;
        border-radius: 30px;
        padding-left: 30px;
        font-size: 16px;
        line-height: 21px;
        color: #808695;
        &:hover,
        &:focus {
          outline: none;
        }
      }
      .search-button {
        position: absolute;
        right: 0;
        z-index: 10;
        font-size: 14px;
        line-height: 14px;
        color: #2a2d54;
        text-transform: uppercase;
        width: 159px;
        height: 48px;
        border-radius: 35px;
        background: linear-gradient(
          180deg,
          #000000 0%,
          #26df07 0.01%,
          #e80202 48.96%,
          #ffe600 100%
        );
        &::after {
          content: "";
          z-index: -1;
          position: absolute;
          top: 2px;
          right: 2px;
          width: 155px;
          height: 44px;
          border-radius: 35px;
          background: linear-gradient(
            101.49deg,
            #a5a8f5 17.34%,
            #b8baf5 53.55%,
            #9296f7 86.43%
          );
        }
      }
    }
  }
}
</style>
