<template>
  <section class="stages section-padding" id="stages">
    <div class="container">
      <h2 class="section-title">
        <span v-if="isEnglish">work stages</span>
        <span v-else>этапы работы</span>
      </h2>
      <ul class="stages__list">
        <li class="card">
          <div class="card__header">
            <span class="card__number">1 /</span>
            <h3 class="card__title">
              <span v-if="isEnglish">Briefing</span>
              <span v-else>Брифинг</span>
            </h3>
          </div>
          <p class="card__info">
            <span v-if="isEnglish">
              I send you an online brief or I call you in a convenient way (we
              will agree on the time in advance) to learn more about your
              company, target audience, competitors, as well as wishes for the
              design and structure of the site.
            </span>
            <span v-else>
              Я отправляю вам онлайн-бриф или мы созваниваемся удобным для вас
              способом (время заранее согласуем), чтобы узнать больше о вашей
              компании, целевой аудитории, конкурентах, а также пожелания по
              оформлению дизайна и структуры сайта.
            </span>
          </p>
        </li>
        <li class="card">
          <div class="card__header">
            <span class="card__number">2 /</span>
            <h3 class="card__title">
              <span v-if="isEnglish">Analytics</span>
              <span v-else>Аналитика</span>
            </h3>
          </div>
          <p class="card__info">
            <span v-if="isEnglish">
              I analyze your company, target audience, competitors, make a site
              map. I select examples of visual solutions and ask you to comment
              on them: what you like and dislike and why.
            </span>
            <span v-else>
              Провожу анализ вашей компании, ЦА, конкурентов, составляю карту
              сайта. Подбираю примеры визуальных решений и прошу вас их
              прокомментировать: что нравится и не нравится и почему.
            </span>
          </p>
        </li>
        <li class="card">
          <div class="card__header">
            <span class="card__number">3 /</span>
            <h3 class="card__title">
              <span v-if="isEnglish">Prototype</span>
              <span v-else>Прототип</span>
            </h3>
          </div>
          <p class="card__info">
            <span v-if="isEnglish">
              I am developing the structure of the future site. Prototype -
              draft, sketch, foundation without design. So that you can
              understand what pages and blocks the site will consist of.
            </span>
            <span v-else>
              Разрабатываю структуру будущего сайта. Прототип – черновик, эскиз,
              фундамент без дизайна. Для того, чтобы вы понимали, из каких
              страниц и блоков будет состоять сайт.
            </span>
          </p>
        </li>
        <li class="card">
          <div class="card__header">
            <span class="card__number">4 /</span>
            <h3 class="card__title">
              <span v-if="isEnglish">Design</span>
              <span v-else>Дизайн</span>
            </h3>
          </div>
          <p class="card__info">
            <span v-if="isEnglish">
              I create a design concept for the site based on your comments and
              approved style.
            </span>
            <span v-else>
              Создаю дизайн-концепцию сайта на основе ваших комментариев и
              утвержденной стилистики.
            </span>
          </p>
        </li>
        <li class="card">
          <div class="card__header">
            <span class="card__number">5 /</span>
            <h3 class="card__title">
              <span v-if="isEnglish">Development</span>
              <span v-else>Верстка</span>
            </h3>
          </div>
          <p class="card__info">
            <span v-if="isEnglish">
              I transfer all previously approved layouts to Tilda, adapt them to
              all devices, animate them, set up the necessary functionality, set
              up basic SEO, bind a domain and an SSL certificate.
            </span>
            <span v-else>
              Я переношу все утвержденные ранее макеты в Тильду, адаптирую их
              под все устройства, анимирую, настраиваю необходимый функционал,
              настраиваю базовое SEO, привязываю домен и SSL-сертификат.
            </span>
          </p>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: "SmnvStages",
  props: {
    isEnglish: {
      type: Boolean,
      required: true,
    },
  },
};
</script>

<style lang="less">
.stages {
  &__list {
    display: flex;
    flex-direction: column;
    gap: 50px;
  }

  .card {
    display: flex;
    gap: 25px;
    padding-top: 15px;
    border-top: 1px solid #a1a1a1;

    @media screen and (max-width: 1199px) {
      flex-direction: column;
    }
    @media screen and (min-width: 1200px) {
      align-items: flex-start;
      justify-content: space-between;
      padding-top: 20px;
    }

    &__header {
      display: flex;
      align-items: center;
      gap: 15px;
      font-size: 20px;
      letter-spacing: -0.02em;
      text-transform: uppercase;

      @media screen and (min-width: 1200px) {
        gap: 409px;
        font-size: 30px;
      }
    }
    &__title {
      font-size: 20px;
      font-weight: 400;

      @media screen and (min-width: 1200px) {
        font-size: 30px;
      }
    }
    &__info {
      font-size: 15px;
      color: #a1a1a1;

      @media screen and (min-width: 1200px) {
        flex-grow: 0;
        flex-shrink: 0;
        flex-basis: 423px;
        font-size: 16px;
      }
    }
  }
}
</style>
