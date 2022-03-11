<template>
  <header class="header" id="top">
    <div class="container header__container">
      <div class="header__lang">
        <button
          type="button"
          :class="['switcher', { _active: isEnglish }]"
          @click="toggleLanguage"
        >
          En
        </button>
        <button
          type="button"
          :class="['switcher', { _active: !isEnglish }]"
          @click="toggleLanguage"
        >
          Ru
        </button>
      </div>
      <div :class="['header__nav', { _active: menuOpened }]">
        <nav class="nav">
          <a href="#portfolio" class="nav__link" @click="handleMenu">
            <span v-if="isEnglish">Portfolio</span>
            <span v-else>Портфолио</span>
          </a>
          <a href="#service" class="nav__link" @click="handleMenu">
            <span v-if="isEnglish">Services</span>
            <span v-else>Услуги</span>
          </a>
          <a href="#stages" class="nav__link" @click="handleMenu">
            <span v-if="isEnglish">Work stages</span>
            <span v-else>Этапы работы</span>
          </a>
          <a href="#contacts" class="nav__link" @click="handleMenu">
            <span v-if="isEnglish">Contacts</span>
            <span v-else>Контакты</span>
          </a>
        </nav>
        <div class="social-links">
          <a
            href="https://www.instagram.com/websmnv/?hl=ru"
            class="social-link"
            target="_blank"
            @click="handleMenu"
          >
            Instagram
          </a>
          <a
            href="tg://resolve?domain=n_smnv"
            class="social-link"
            target="_blank"
            @click="handleMenu"
          >
            Telegram
          </a>
          <a
            href="https://www.behance.net/nataliasemenova"
            class="social-link"
            target="_blank"
            @click="handleMenu"
          >
            Behance
          </a>
        </div>
      </div>
      <button
        type="button"
        :class="['header__burger', { _active: menuOpened }]"
        @click="handleMenu"
      >
        <span class="line line--top"></span>
        <span class="line line--bottom"></span>
      </button>
    </div>
  </header>
</template>

<script>
export default {
  name: "SmnvHeader",
  props: {
    isEnglish: {
      type: Boolean,
      required: true,
    },
  },
  emits: ["toggle-language"],
  data() {
    return {
      menuOpened: false,
    };
  },
  methods: {
    handleMenu() {
      this.menuOpened = !this.menuOpened;
    },
    toggleLanguage() {
      this.$emit("toggle-language");
    },
  },
};
</script>

<style lang="less">
.header {
  padding-top: 30px;
  &__container {
    display: flex;
    align-items: center;
    justify-content: space-between;

    @media screen and (min-width: 1200px) {
      flex-direction: row-reverse;
      gap: 105px;
    }
  }
  &__lang {
    position: relative;
    display: flex;
    gap: 15px;
    z-index: 10;

    .switcher {
      font-size: 14px;
      line-height: 1;
      text-transform: uppercase;
      color: #fff;
      transition: color 0.3s ease-in-out;

      &:hover {
        color: #a1a1a1;
      }

      &._active {
        text-decoration: underline;
      }
    }
  }
  &__nav {
    display: flex;
    align-items: center;
    justify-content: space-between;

    &._active {
      opacity: 1;
      transform: scale(1);
      z-index: 1;
    }

    .nav {
      display: flex;
      align-items: center;
      gap: 20px;
      &__link {
        font-size: 20px;
        line-height: 24px;
        text-transform: uppercase;
        color: #fff;
        transition: color 0.3s ease-in-out;

        &:hover {
          color: #a1a1a1;
        }

        @media screen and (min-width: 1200px) {
          font-size: 14px;
          line-height: 17px;
        }
      }

      @media screen and (max-width: 1199px) {
        flex-direction: column;
      }
    }
    .social-links {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 33px;

      @media screen and (min-width: 1200px) {
        gap: 20px;
      }
    }
    .social-link {
      font-size: 14px;
      line-height: 1.3;
      color: #fff;
      text-transform: uppercase;
      text-decoration: underline;
      transition: color 0.3s ease-in-out;

      &:hover {
        color: #a1a1a1;
      }
    }
    @media screen and (max-width: 1199px) {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      flex-direction: column;
      opacity: 0;
      padding: 160px 15px 30px;
      transform: scale(0.9);
      transition: opacity 0.2s ease-in-out, transform 0.3s ease-in-out;
      z-index: -1;
    }
    @media screen and (min-width: 1200px) {
      flex-grow: 1;
    }
  }
  &__burger {
    position: relative;
    width: 28px;
    display: flex;
    flex-direction: column;
    gap: 10px;
    z-index: 10;

    .line {
      width: 100%;
      height: 2px;
      background-color: #fff;
      transform: translateY(0px);
      transition: transform 0.3s ease-in-out;
    }
    &._active {
      .line--top {
        transform: translateY(6px) rotate(45deg);
      }
      .line--bottom {
        transform: translateY(-6px) rotate(-45deg);
      }
    }

    @media screen and (min-width: 1200px) {
      display: none;
    }
  }
}
</style>
