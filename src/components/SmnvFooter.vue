<template>
  <footer class="footer">
    <div class="container">
      <div class="footer__body">
        <div class="footer__name">Natalia Semenova 2022</div>
        <a href="#top" class="footer__top">
          <span v-if="isEnglish">Back to top</span>
          <span v-else>Наверх</span>
          <svg
            width="10"
            height="9"
            viewBox="0 0 14 13"
            xmlns="http://www.w3.org/2000/svg"
          >
            <use href="#arrow" />
          </svg>
        </a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "SmnvFooter",
  props: {
    isEnglish: {
      type: Boolean,
      required: true,
    },
  },
};
</script>

<style lang="less">
.footer {
  padding-top: 80px;
  padding-bottom: 30px;

  @media screen and (min-width: 1200px) {
    padding-top: 200px;
    padding-bottom: 42px;
  }

  &__body {
    display: flex;
    align-items: flex-end;
    justify-content: space-between;
    padding-top: 15px;
    border-top: 1px solid #a1a1a1;

    @media screen and (min-width: 1200px) {
      padding-top: 20px;
    }
  }
  &__name {
    font-size: 15px;

    @media screen and (max-width: 1199px) {
      flex-basis: 125px;
    }
    @media screen and (min-width: 1200px) {
      font-size: 16px;
    }
  }
  &__top {
    position: relative;
    font-size: 15px;
    color: #fff;
    padding-right: 16px;
    transition: color 0.3s ease-in-out;

    &:hover {
      color: #a1a1a1;

      svg {
        fill: #a1a1a1;
      }
    }

    svg {
      position: absolute;
      right: 0;
      bottom: 6px;
      fill: #fff;
      transform: rotate(-45deg);
      transition: fill 0.3s ease-in-out;
    }

    @media screen and (min-width: 1200px) {
      font-size: 16px;
    }
  }
}
</style>
