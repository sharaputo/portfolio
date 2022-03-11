<template>
  <section class="portfolio" id="portfolio">
    <div class="container">
      <h2 class="section-title">
        <span v-if="isEnglish">portfolio</span>
        <span v-else>портфолио</span>
      </h2>
      <div class="portfolio__body">
        <ul class="portfolio__list">
          <li class="portfolio__item">
            <a href="#!" class="card card--upcoming">
              <div class="card__image">
                <img
                  class="card__img"
                  alt=""
                  src="./../assets/portfolio/portfolio-1.jpg"
                />
                <div class="label">
                  <span v-if="isEnglish">Soon</span>
                  <span v-else>Скоро</span>
                </div>
              </div>
              <div class="card__title">
                <span v-if="isEnglish">Longread of Vogue Dance History</span>
                <span v-else>Лонгрид истории танца Вог</span>
                <svg
                  width="14"
                  height="13"
                  viewBox="0 0 14 13"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <use href="#arrow" />
                </svg>
              </div>
            </a>
          </li>
          <li class="portfolio__item">
            <a
              href="https://xn--80ahbenfd7azbosd7e.xn--p1ai/"
              class="card"
              target="_blank"
            >
              <img
                class="card__img"
                alt=""
                src="./../assets/portfolio/portfolio-2.jpg"
              />
              <div class="card__title">
                <span v-if="isEnglish">Franchise landing page</span>
                <span v-else>Лендинг для франшизы</span>
                <svg
                  width="14"
                  height="13"
                  viewBox="0 0 14 13"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <use href="#arrow" />
                </svg>
              </div>
            </a>
          </li>
          <li class="portfolio__item">
            <a href="https://lova-dsgn.com/" class="card" target="_blank">
              <img
                class="card__img"
                alt=""
                src="./../assets/portfolio/portfolio-3.jpg"
              />
              <div class="card__title">
                <span v-if="isEnglish">Website for a brand design studio</span>
                <span v-else>Сайт для студии бренд-дизайна</span>
                <svg
                  width="14"
                  height="13"
                  viewBox="0 0 14 13"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <use href="#arrow" />
                </svg>
              </div>
            </a>
          </li>
        </ul>
        <ul class="portfolio__list">
          <li class="portfolio__item">
            <a href="#!" class="card card--upcoming">
              <div class="card__image">
                <img
                  class="card__img"
                  alt=""
                  src="./../assets/portfolio/portfolio-4.jpg"
                />
                <div class="label">
                  <span v-if="isEnglish">Soon</span>
                  <span v-else>Скоро</span>
                </div>
              </div>
              <div class="card__title">
                <span v-if="isEnglish">
                  Website for architecture and design bureau
                </span>
                <span v-else>Сайт для бюро архитектуры и дизайна</span>
                <svg
                  width="14"
                  height="13"
                  viewBox="0 0 14 13"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <use href="#arrow" />
                </svg>
              </div>
            </a>
          </li>
          <li class="portfolio__item">
            <a href="https://artandsweets.ru/" class="card" target="_blank">
              <img
                class="card__img"
                alt=""
                src="./../assets/portfolio/portfolio-5.jpg"
              />
              <div class="card__title">
                <span v-if="isEnglish">Website for a confectionery</span>
                <span v-else>Сайт для кондитерской</span>
                <svg
                  width="14"
                  height="13"
                  viewBox="0 0 14 13"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <use href="#arrow" />
                </svg>
              </div>
            </a>
          </li>
          <li class="portfolio__item">
            <a
              href="https://www.behance.net/gallery/127815777/Website-for-an-online-school-%28energy-meditation%29"
              class="card"
              target="_blank"
            >
              <img
                class="card__img"
                alt=""
                src="./../assets/portfolio/portfolio-6.jpg"
              />
              <div class="card__title">
                <span v-if="isEnglish">
                  Website for the School of Energy Practitioners
                </span>
                <span v-else>Сайт для школы энергопрактик</span>
                <svg
                  width="14"
                  height="13"
                  viewBox="0 0 14 13"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <use href="#arrow" />
                </svg>
              </div>
            </a>
          </li>
        </ul>
        <ul class="portfolio__list">
          <li class="portfolio__item">
            <a href="#!" class="card card--upcoming">
              <div class="card__image">
                <img
                  class="card__img"
                  alt=""
                  src="./../assets/portfolio/portfolio-7.jpg"
                />
                <div class="label">
                  <span v-if="isEnglish">Soon</span>
                  <span v-else>Скоро</span>
                </div>
              </div>
              <div class="card__title">
                <span v-if="isEnglish">
                  Website for a permanent makeup artist
                </span>
                <span v-else>Сайт для мастера перманентного макияжа</span>
                <svg
                  width="14"
                  height="13"
                  viewBox="0 0 14 13"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <use href="#arrow" />
                </svg>
              </div>
            </a>
          </li>
          <li class="portfolio__item">
            <a
              href="https://www.behance.net/gallery/117642335/Wellness-center-Uweya-website-design-yoga-meditation"
              class="card"
              target="_blank"
            >
              <img
                class="card__img"
                alt=""
                src="./../assets/portfolio/portfolio-8.jpg"
              />
              <div class="card__title">
                <span v-if="isEnglish">Website for a wellness center</span>
                <span v-else>Сайт для оздоровительного центра</span>
                <svg
                  width="14"
                  height="13"
                  viewBox="0 0 14 13"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <use href="#arrow" />
                </svg>
              </div>
            </a>
          </li>
          <li class="portfolio__item">
            <a
              href="https://www.behance.net/gallery/116699961/Safisa-organic-skincare-cosmetics-e-commerce"
              class="card"
              target="_blank"
            >
              <img
                class="card__img"
                alt=""
                src="./../assets/portfolio/portfolio-9.jpg"
              />
              <div class="card__title">
                <span v-if="isEnglish">
                  Online store of skin care cosmetics
                </span>
                <span v-else>Интернет-магазин уходовой косметики</span>
                <svg
                  width="14"
                  height="13"
                  viewBox="0 0 14 13"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <use href="#arrow" />
                </svg>
              </div>
            </a>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "SmnvPortfolio",
  props: {
    isEnglish: {
      type: Boolean,
      required: true,
    },
  },
};
</script>

<style lang="less">
.portfolio {
  padding-top: 80px;

  @media screen and (min-width: 1200px) {
    padding-top: 205px;
  }
  &__body {
    display: flex;

    @media screen and (max-width: 1199px) {
      flex-direction: column;
      gap: 40px;
    }
    @media screen and (min-width: 1200px) {
      gap: 24px;
    }
  }
  &__list {
    display: flex;
    flex-direction: column;
    gap: 40px;

    @media screen and (min-width: 1200px) {
      gap: 50px;
    }
  }

  .card {
    display: block;
    color: #fff;
    padding-bottom: 10px;
    border-bottom: 1px solid #a1a1a1;

    &__image {
      position: relative;
    }
    &__img {
      filter: grayscale(1);
      transition: filter 0.3s ease-in-out;
    }
    &__title {
      display: flex;
      align-items: flex-end;
      justify-content: space-between;
      font-size: 15px;
      letter-spacing: -0.02em;
      margin-top: 15px;
      transition: color 0.3s ease-in-out;

      svg {
        fill: #fff;
        margin-bottom: 3px;
        transition: fill 0.3s ease-in-out;
      }

      @media screen and (min-width: 1200px) {
        font-size: 16px;
        margin-top: 20px;
      }
    }
    .label {
      position: absolute;
      top: calc(50% - 44px);
      left: calc(50% - 44px);
      width: 89px;
      height: 89px;
      display: grid;
      place-items: center;
      font-size: 16px;
      font-weight: 300;
      text-align: center;
      letter-spacing: -0.02em;
      color: #201f1f;
      background-color: #fff;
      border-radius: 50%;
    }

    &:hover:not(.card--upcoming) {
      .card__img {
        filter: grayscale(0);
      }
      .card__title {
        color: #a1a1a1;
      }
      svg {
        fill: #a1a1a1;
      }
    }

    @media screen and (min-width: 1200px) {
      padding-bottom: 15px;
    }
  }
}
</style>
