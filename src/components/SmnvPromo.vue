<template>
  <section class="promo">
    <div class="container">
      <h1 class="promo__title">
        <span class="english" v-if="isEnglish">Web design & sites</span>
        <span v-else>Веб-дизайн & сайты</span>
      </h1>
      <div class="promo__body">
        <div class="promo__info">
          <p class="info">
            <span v-if="isEnglish">
              Hello! I'm Natalia. I develop websites on Tilda platform and I
              also design websites for other platforms. I'm sure that design is
              not only about appearance, but also about convenience and
              functionality. The end result of my work is neat, clean and
              responsive web product that works.
            </span>
            <span v-else>
              Здравствуйте! Меня зовут Наталья. Я разрабатываю сайты на Tilda, а
              также создаю дизайн сайтов под другие платформы. Я уверена, что
              дизайн – это не только внешний вид, но и удобство и
              функциональность. Конечным результатом моей работы является
              аккуратный, чистый и отзывчивый веб-продукт, который работает.
            </span>
          </p>
          <ul class="tags">
            <li class="tag">
              <span v-if="isEnglish">web design</span>
              <span v-else>веб-дизайн</span>
            </li>
            <li class="tag">
              <span v-if="isEnglish">websites</span>
              <span v-else>сайты</span>
            </li>
            <li class="tag tag--mobile">
              <span>tilda</span>
            </li>
          </ul>
          <a
            :href="
              isEnglish
                ? 'https://docs.google.com/forms/d/e/1FAIpQLSeOfcCLaOei1hR-935rW36bM5uRZy94nIIM9-Qa3TD-Gmustw/viewform'
                : 'https://docs.google.com/forms/d/e/1FAIpQLSe-HPYDxVZKD84IA5-YhDaWdueha5ivqTz7_JR807QmXRQWNw/viewform'
            "
            class="brief"
            target="_blank"
          >
            <svg
              width="14"
              height="13"
              viewBox="0 0 14 13"
              xmlns="http://www.w3.org/2000/svg"
            >
              <use href="#arrow" />
            </svg>
            <span v-if="isEnglish">fill brief</span>
            <span v-else>заполнить бриф</span>
          </a>
        </div>
        <div class="promo__photo">
          <img alt="Natalia Semenova" src="./../assets/promo.jpg" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "SmnvPromo",
  props: {
    isEnglish: {
      type: Boolean,
      required: true,
    },
  },
};
</script>

<style lang="less">
.promo {
  padding-top: 50px;
  &__title {
    font-size: 53px;
    font-weight: 300;
    line-height: 1.14;
    letter-spacing: -0.02em;
    text-transform: uppercase;
    margin-bottom: 30px;

    .english {
      @media screen and (min-width: 1200px) {
        font-size: 135px;
        line-height: 0.95;
      }
    }

    @media screen and (max-width: 1199px) {
      max-width: 260px;
    }
    @media screen and (min-width: 1200px) {
      font-size: 119px;
      line-height: 1.3;
      margin-bottom: 78px;
    }
  }
  &__body {
    display: flex;
    gap: 40px;

    @media screen and (max-width: 1199px) {
      flex-direction: column;
    }
    @media screen and (min-width: 1200px) {
      justify-content: space-between;
    }
  }
  &__info {
    @media screen and (min-width: 1200px) {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      flex-grow: 0;
      flex-basis: 423px;
    }
  }
  &__photo {
    @media screen and (min-width: 1200px) {
      flex-grow: 0;
      flex-shrink: 0;
      flex-basis: 423px;
    }
  }

  .info {
    font-size: 15px;
    color: #a1a1a1;
    margin-bottom: 40px;

    @media screen and (min-width: 1200px) {
      font-size: 16px;
      margin-bottom: 50px;
    }
  }
  .tags {
    display: flex;
    align-items: center;
    gap: 20px;
    margin-bottom: 40px;
  }
  .tag {
    font-size: 14px;
    line-height: 1.17;
    text-transform: uppercase;
    padding: 8px 20px;
    border: 1px solid #fff;
    border-radius: 38px;
  }
  .tag--mobile {
    @media screen and (max-width: 1199px) {
      display: none;
    }
  }
  .brief {
    position: relative;
    font-size: 20px;
    text-transform: uppercase;
    color: #fff;
    padding-bottom: 7px;
    padding-left: 22px;
    transition: color 0.3s ease-in-out;
    &::after {
      display: block;
      content: "";
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 2px;
      background-color: #fff;
      transition: background-color 0.3s ease-in-out;
    }
    &:hover {
      color: #a1a1a1;
      &::after {
        background-color: #a1a1a1;
      }
      svg {
        fill: #a1a1a1;
      }
    }

    svg {
      position: absolute;
      top: 5px;
      left: 0;
      fill: #fff;
      transition: fill 0.3s ease-in-out;
    }

    @media screen and (min-width: 1200px) {
      margin-top: auto;
    }
  }

  @media screen and (max-width: 1199px) {
  }
  @media screen and (min-width: 1200px) {
    padding-top: 63px;
  }
}
</style>
