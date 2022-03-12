<template>
  <section class="costs section-padding">
    <div class="container">
      <h2 class="section-title costs__title">
        <span v-if="isEnglish">additional costs for the site</span>
        <span v-else>доп. расходы для сайта</span>
      </h2>
      <SmnvAccordion>
        <SmnvAccordionItem>
          <template v-slot:accordion-trigger>
            <h3>
              <span v-if="isEnglish">Account</span>
              <span v-else>Аккаунт</span>
            </h3>
          </template>
          <template v-slot:accordion-content>
            <p>
              <span v-if="isEnglish">
                Tilda has hosting called Personal (for one site) that costs $15
                per month. If you buy for a full year, it will cost $120 per
                year. If you plan to host several sites, then the Business plan
                is suitable ($25 per month and $240 per year).
              </span>
              <span v-else>
                У Tilda есть хостинг Personal (на один сайт) стоит $15/мес, если
                покупать на год, то $120/год. Если вы планируете размещать
                несколько сайтов, то подойдёт тариф Business ($25/мес, если
                покупать на год, то $240/год).
              </span>
            </p>
          </template>
        </SmnvAccordionItem>

        <SmnvAccordionItem>
          <template v-slot:accordion-trigger>
            <h3>
              <span v-if="isEnglish">Domain</span>
              <span v-else>Домен</span>
            </h3>
          </template>
          <template v-slot:accordion-content>
            <p>
              <span v-if="isEnglish">
                You can get your domen on Tilda platform. The first year is free
                if you pay yearly Personal or Business subscription. After a
                year, the domain price can be renewed at the usual registrar's
                tariff (reg.ru).
              </span>
              <span v-else>
                Можно оформить прямо на Тильде. Первый год они дают его в
                подарок (при условии, если вы купите годовой тариф Personal или
                Business). Через год стоимость домена можно продлить по обычному
                тарифу регистратора (РЕГ.РУ).
              </span>
            </p>
          </template>
        </SmnvAccordionItem>

        <SmnvAccordionItem>
          <template v-slot:accordion-trigger>
            <h3>
              <span v-if="isEnglish">Photo and video shooting</span>
              <span v-else>Фото и видеосъёмка</span>
            </h3>
          </template>
          <template v-slot:accordion-content>
            <p>
              <span v-if="isEnglish">
                If you don't have any ready-made graphics or it's outdated, I
                can pick up photos/videos from free stocks. But I still
                recommend using the services of a photographer or images from
                paid resources.<br />
                Why? Because the photographer or videographer will create unique
                content that no one else has. In addition, the content will
                fully comply with the requirements of the company.
              </span>
              <span v-else>
                Если у вас совсем нет готовой графики или она устарела, я могу
                подобрать фото/видео из бесплатных стоков. Но рекомендую всё же
                использовать услуги фотографа или изображения из платных
                ресурсов.<br />
                Почему? Потому что фотограф или видеограф создаст уникальный
                контент, которого больше ни у кого нет. К тому же, контент будет
                полностью соответствовать требованиям компании.
              </span>
            </p>
          </template>
        </SmnvAccordionItem>

        <SmnvAccordionItem>
          <template v-slot:accordion-trigger>
            <h3>
              <span v-if="isEnglish">Complex copywriting</span>
              <span v-else>Сложный копирайтинг</span>
            </h3>
          </template>
          <template v-slot:accordion-content>
            <p>
              <span v-if="isEnglish">
                I arrange the sent text content into a single structure, if
                necessary, I rewrite the finished text.
              </span>
              <span v-else>
                Я оформляю присланный текстовый контент в единую структуру, при
                необходимости делаю рерайт готового текста.
              </span>
            </p>
          </template>
        </SmnvAccordionItem>

        <SmnvAccordionItem>
          <template v-slot:accordion-trigger>
            <h3>
              <span v-if="isEnglish">Fonts</span>
              <span v-else>Шрифты</span>
            </h3>
          </template>
          <template v-slot:accordion-content>
            <p>
              <span v-if="isEnglish">
                There are both free and paid fonts. Among the free fonts there
                are a lot of cool ones, there are quite enough of them. But if
                you want individuality, you can purchase a paid option. The
                price is indicated for one style, two or three are enough for
                the site.
              </span>
              <span v-else>
                Есть как бесплатные, так и платные шрифты. Среди бесплатных
                шрифтов есть очень много классных, их вполне хватает. Но если
                хочется индивидуальности, то можно приобрести платный вариант.
                Цена указывается за одно начертание, для сайта вполне хватит
                двух-трёх.
              </span>
            </p>
          </template>
        </SmnvAccordionItem>

        <SmnvAccordionItem>
          <template v-slot:accordion-trigger>
            <h3>
              <span v-if="isEnglish">Website promotion</span>
              <span v-else>Продвижение сайта</span>
            </h3>
          </template>
          <template v-slot:accordion-content>
            <p>
              <span v-if="isEnglish">
                I only do basic SEO setup — I optimize images, set up headings,
                open the site for search engines, add the site to
                Yandex.Webmaster and Google.Console. Further promotion is
                handled by a SEO specialist.
              </span>
              <span v-else>
                Я делаю только базовую настройку SEO — оптимизирую изображения,
                настраиваю заголовки, открываю сайт для поисковиков, добавляю
                сайт в Яндекс.Вебмастер и Google.Console. Дальнейшим
                продвижением занимается SEO-специалист.
              </span>
            </p>
          </template>
        </SmnvAccordionItem>
      </SmnvAccordion>
    </div>
  </section>
</template>

<script>
import SmnvAccordion from "./accordion/SmnvAccordion.vue";
import SmnvAccordionItem from "./accordion/SmnvAccordionItem";

export default {
  name: "SmnvCosts",
  components: {
    SmnvAccordion,
    SmnvAccordionItem,
  },
  props: {
    isEnglish: {
      type: Boolean,
      required: true,
    },
  },
  data() {
    return {
      index: null,
      Accordion: {
        count: 0,
        active: null,
      },
    };
  },
  computed: {
    visible() {
      return this.index == this.Accordion.active;
    },
  },
  methods: {
    open() {
      if (this.visible) {
        this.Accordion.active = null;
      } else {
        this.Accordion.active = this.index;
      }
    },
    start(el) {
      el.style.height = el.scrollHeight + "px";
    },
    end(el) {
      el.style.height = "";
    },
  },
  created() {
    this.index = this.Accordion.count++;
  },
};
</script>

<style lang="less">
.costs {
  &__title {
    @media screen and (min-width: 1200px) {
      max-width: 900px;
    }
  }
}
</style>
