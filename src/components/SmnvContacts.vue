<template>
  <section class="contacts section-padding" id="contacts">
    <div class="container">
      <h2 class="section-title">
        <span v-if="isEnglish">contacts</span>
        <span v-else>контакты</span>
      </h2>
      <div class="contacts__body">
        <ul class="contacts__links">
          <li class="contacts__link">
            <a
              href="https://www.instagram.com/websmnv/?hl=ru"
              class="contact"
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
              Instagram
            </a>
          </li>
          <li class="contacts__link">
            <a
              href="https://www.behance.net/nataliasemenova"
              class="contact"
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
              Behance
            </a>
          </li>
          <li class="contacts__link">
            <a
              href="tg://resolve?domain=n_smnv"
              class="contact"
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
              Telegram
            </a>
          </li>
          <li class="contacts__link">
            <a href="https://wa.me/79213360423" class="contact" target="_blank">
              <svg
                width="14"
                height="13"
                viewBox="0 0 14 13"
                xmlns="http://www.w3.org/2000/svg"
              >
                <use href="#arrow" />
              </svg>
              Whatsapp
            </a>
          </li>
        </ul>
        <a
          :href="
            isEnglish
              ? 'https://docs.google.com/forms/d/e/1FAIpQLSeOfcCLaOei1hR-935rW36bM5uRZy94nIIM9-Qa3TD-Gmustw/viewform'
              : 'https://docs.google.com/forms/d/e/1FAIpQLSe-HPYDxVZKD84IA5-YhDaWdueha5ivqTz7_JR807QmXRQWNw/viewform'
          "
          class="contacts__brief"
          target="_blank"
        >
          <span v-if="isEnglish">fill brief</span>
          <span v-else>заполнить бриф</span>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "SmnvContacts",
  props: {
    isEnglish: {
      type: Boolean,
      required: true,
    },
  },
};
</script>

<style lang="less">
.contacts {
  &__body {
    display: flex;
    align-items: center;
    gap: 40px;

    @media screen and (max-width: 1199px) {
      flex-direction: column;
    }
    @media screen and (min-width: 1200px) {
      justify-content: space-between;
    }
  }
  &__links {
    display: grid;
    grid-template-columns: 1fr 1fr;
    column-gap: 13px;
    row-gap: 24px;
    .contact {
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

      svg {
        position: absolute;
        top: 5px;
        left: 0;
        fill: #fff;
        transition: fill 0.3s ease-in-out;

        @media screen and (min-width: 1200px) {
          top: 8px;
          width: 18px;
          height: 17px;
        }
      }

      @media screen and (min-width: 1200px) {
        font-size: 30px;
        padding-left: 29px;
      }
    }

    @media screen and (max-width: 1199px) {
      width: 100%;
    }
    @media screen and (min-width: 1200px) {
      column-gap: 258px;
      row-gap: 52px;
    }
  }
  &__brief {
    width: 100%;
    font-size: 18px;
    text-align: center;
    text-transform: uppercase;
    color: #201f1f;
    background: #fff;
    padding: 32px 0;
    border: 1px solid #fff;
    border-radius: 78px;
    transition: color 0.3s ease-in-out, background-color 0.3s ease-in-out;

    @media screen and (min-width: 1200px) {
      flex-grow: 0;
      flex-shrink: 0;
      flex-basis: 423px;
      font-size: 20px;
      padding: 50px 0;
    }
  }
}
</style>
