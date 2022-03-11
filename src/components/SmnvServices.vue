<template>
  <section class="services" id="service">
    <div class="container">
      <h2 class="section-title">
        <span v-if="isEnglish">services</span>
        <span v-else>услуги</span>
      </h2>
      <ul class="services__list">
        <li class="services__item">
          <div class="service">
            <h3 class="service__title">
              <span v-if="isEnglish">Landing page</span>
              <span v-else>Лендинг</span>
            </h3>
            <p class="service__info">
              <span v-if="isEnglish">
                A small one-page site that calls the user to action: order a
                product or service, call the manager, leave a request. Such a
                site contains feedback form, information about the product,
                discounts, special offers. The landing page is perfect for
                webinars, info products, events, etc.
              </span>
              <span v-else>
                Небольшой одностраничный сайт, который призывает пользователя к
                действию: заказать товар или услугу, позвонить менеджеру,
                оставить заявку. На таком сайте размещают информацию о продукте,
                скидках, спец. предложениях, форму обратной связи. Лендинг
                отлично подойдёт для вебинаров, инфо-продуктов, мероприятий и
                т.д.
              </span>
            </p>
            <div class="service__details">
              <div class="service__price">
                <span class="label" v-if="isEnglish">from</span>
                <span class="label" v-else>от</span>
                <span class="price">$400</span>
              </div>
              <div class="service__time">
                <span v-if="isEnglish">(up to 14 days)</span>
                <span v-else>(до 14 дней)</span>
              </div>
            </div>
          </div>
        </li>
        <li class="services__item">
          <div class="service">
            <h3 class="service__title">
              <span v-if="isEnglish">Multipage site</span>
              <span v-else>Многостраничный сайт</span>
            </h3>
            <p class="service__info">
              <span v-if="isEnglish">
                A site with a more complex structure. It contains detailed
                information about the company, goods/services, site search,
                photo/video materials, certificates, reviews, blog, contacts,
                etc. Such a site is suitable for large companies that need not
                only sales, but also building a reputation online, searching for
                investors and partners.
              </span>
              <span v-else>
                Сайт с более сложной структурой. На нём размещается развёрнутая
                информация о компании, товарах/услугах, поиск по сайту,
                фото/видео-материалы, сертификаты, отзывы, блог, контакты и т.д.
                Такой сайт подойдёт крупным компаниям, которым нужны не только
                продажи, но и построение репутации в онлайне, поиск инвесторов и
                партнёров.
              </span>
            </p>
            <div class="service__details">
              <div class="service__price">
                <span class="label" v-if="isEnglish">from</span>
                <span class="label" v-else>от</span>
                <span class="price">$600</span>
              </div>
              <div class="service__time">
                <span v-if="isEnglish">(from 14 days)</span>
                <span v-else>(от 14 дней)</span>
              </div>
            </div>
          </div>
        </li>
        <li class="services__item">
          <div class="service">
            <h3 class="service__title">
              <span v-if="isEnglish">E-commerce</span>
              <span v-else>Интернет-магазин</span>
            </h3>
            <p class="service__info">
              <span v-if="isEnglish">
                A site that contains a catalog with products, their detailed
                description, photos and prices, a shopping cart, an online
                payment system and notifications of the seller and buyer about
                the order. An online store is suitable for those who offer a
                wide range of goods or services and want to expand their sales
                by going online.
              </span>
              <span v-else>
                Сайт, который содержит каталог с товарами, его подробным
                описанием, фотографиями и ценами, корзиной, системой
                онлайн-оплаты и уведомлением продавца и покупателя о заказе.
                Интернет-магазин подойдёт тем, кто предлагает широкий
                ассортимент товаров или услуг и хочет расширить продажи, перейдя
                в онлайн.
              </span>
            </p>
            <div class="service__details">
              <div class="service__price">
                <span class="label" v-if="isEnglish">from</span>
                <span class="label" v-else>от</span>
                <span class="price">$800</span>
              </div>
              <div class="service__time">
                <span v-if="isEnglish">(from 14 days)</span>
                <span v-else>(от 14 дней)</span>
              </div>
            </div>
          </div>
        </li>
        <li class="services__item">
          <div class="service">
            <h3 class="service__title">
              <span v-if="isEnglish">Website design in Figma</span>
              <span v-else>Дизайн сайта в Figma</span>
            </h3>
            <p class="service__info">
              <span v-if="isEnglish">
                Development of a design layout of the site for further transfer
                to web developer.
              </span>
              <span v-else>
                Разработка дизайн-макета сайта для дальнейшей передачи его
                верстальщику.
              </span>
            </p>
            <div class="service__details">
              <div class="service__price">
                <span class="label" v-if="isEnglish">from</span>
                <span class="label" v-else>от</span>
                <span class="price">$200</span>
              </div>
              <div class="service__time">
                <span v-if="isEnglish">(from 7 days)</span>
                <span v-else>(от 7 дней)</span>
              </div>
            </div>
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: "SmnvServices",
  props: {
    isEnglish: {
      type: Boolean,
      required: true,
    },
  },
};
</script>

<style lang="less">
.services {
  padding-top: 80px;

  @media screen and (min-width: 1200px) {
    padding-top: 200px;
  }
  &__list {
    display: flex;
    flex-direction: column;
    gap: 50px;
  }

  .service {
    display: flex;
    justify-content: space-between;
    gap: 25px;
    padding-top: 15px;
    border-top: 1px solid #a1a1a1;

    @media screen and (max-width: 1199px) {
      flex-direction: column;
    }
    @media screen and (min-width: 1200px) {
      align-items: flex-start;
      padding-top: 24px;
    }

    &__title {
      font-size: 20px;
      font-weight: 400;
      letter-spacing: -0.02em;
      text-transform: uppercase;

      @media screen and (min-width: 1200px) {
        flex-grow: 0;
        flex-shrink: 0;
        flex-basis: 325px;
        font-size: 30px;
      }
    }
    &__info {
      font-size: 15px;
      color: #a1a1a1;

      @media screen and (min-width: 1200px) {
        flex-grow: 0;
        flex-shrink: 0;
        flex-basis: 425px;
        font-size: 16px;
      }
    }
    &__details {
      display: flex;
      align-items: flex-end;
      @media screen and (max-width: 1199px) {
        justify-content: space-between;
      }
      @media screen and (min-width: 1200px) {
        flex-direction: column;
        gap: 15px;
      }
    }
    &__price {
      display: flex;
      gap: 8px;
      .label {
        font-size: 15px;
        line-height: 1;

        @media screen and (min-width: 1200px) {
          font-size: 16px;
          line-height: 1.31;
        }
      }
      .price {
        font-size: 20px;
        line-height: 0.95;
        letter-spacing: -0.02em;
        text-transform: uppercase;

        @media screen and (min-width: 1200px) {
          font-size: 40px;
        }
      }

      @media screen and (max-width: 1199px) {
        align-items: flex-end;
      }
    }
    &__time {
      font-size: 15px;
      line-height: 1.31;
      color: #a1a1a1;

      @media screen and (min-width: 1200px) {
        font-size: 16px;
      }
    }
  }
}
</style>
