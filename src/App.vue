<template>
  <SmnvHeader :is-english="isEnglish" @toggle-language="switchLanguage" />

  <main>
    <SmnvPromo :is-english="isEnglish" />
    <SmnvServices :is-english="isEnglish" />
    <SmnvPortfolio :is-english="isEnglish" />
    <SmnvStages :is-english="isEnglish" />
    <SmnvCosts :is-english="isEnglish" />
    <SmnvContacts :is-english="isEnglish" />
  </main>

  <SmnvFooter :is-english="isEnglish" />
</template>

<script>
import SmnvHeader from "./components/SmnvHeader.vue";
import SmnvPromo from "./components/SmnvPromo.vue";
import SmnvServices from "./components/SmnvServices.vue";
import SmnvPortfolio from "./components/SmnvPortfolio.vue";
import SmnvStages from "./components/SmnvStages.vue";
import SmnvCosts from "./components/SmnvCosts.vue";
import SmnvContacts from "./components/SmnvContacts.vue";
import SmnvFooter from "./components/SmnvFooter.vue";

export default {
  name: "App",
  components: {
    SmnvHeader,
    SmnvPromo,
    SmnvServices,
    SmnvPortfolio,
    SmnvStages,
    SmnvCosts,
    SmnvContacts,
    SmnvFooter,
  },
  data() {
    return {
      isEnglish: true,
    };
  },
  created() {
    this.setLanguage();
  },
  methods: {
    switchLanguage() {
      this.isEnglish = !this.isEnglish;
    },
    setLanguage() {
      const lang = navigator.language;

      if (lang === "ru-RU") {
        this.isEnglish = false;
      } else {
        this.isEnglish = true;
      }
    },
  },
};
</script>

<style lang="less">
* {
  padding: 0;
  margin: 0;
  border: 0;
}
*,
*:before,
*:after {
  box-sizing: border-box;
}
:focus,
:active {
  outline: none;
}
::-webkit-file-upload-button {
  font: inherit;
  -webkit-appearance: button;
}
[role="button"] {
  cursor: pointer;
}
[tabindex="-1"]:focus:not(:focus-visible) {
  outline: 0 !important;
}
a:active,
a:focus {
  outline: none;
}
a,
a:hover,
a:visited {
  text-decoration: none;
}
a,
button {
  -webkit-tap-highlight-color: transparent;
}
footer,
header,
main,
nav,
section {
  display: block;
}
button {
  font-family: inherit;
  line-height: inherit;
  text-transform: none;
  background: transparent;
  padding: 0;
  border: none;
  border-radius: 0;
  outline: none;
  padding: 0;
  margin: 0;
  overflow: visible;
  cursor: pointer;
  &:focus {
    outline: none;
  }
}
button::-moz-focus-inner {
  padding: 0;
  border: 0;
}
button,
[type="button"] {
  -webkit-appearance: button;
}
button,
[type="button"] {
  &:not(:disabled) {
    cursor: pointer;
  }
}
button::-moz-focus-inner,
[type="button"]::-moz-focus-inner {
  padding: 0;
  border-style: none;
}
img,
svg {
  max-width: 100%;
  height: auto;
  vertical-align: top;
}
img[src$=".svg"] {
  max-width: none;
  width: 100%;
  height: auto;
}
h1,
h2,
h3,
h4,
h5,
h6 {
  margin-top: 0;
  margin-bottom: 0;
}
html,
body {
  -ms-text-size-adjust: 100%;
  -moz-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  scroll-behavior: smooth;
}
p {
  margin-top: 0;
  margin-bottom: 0;
}
ul {
  margin-top: 0;
  margin-bottom: 0;
}
ul li {
  list-style: none;
}

body {
  width: 100%;
  min-width: 320px;
  font-family: "Inter", sans-serif;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 1.35;
  word-wrap: break-word;
  overflow-wrap: break-word;
  font-feature-settings: "tnum" on, "lnum" on;
  color: #fff;
  background-color: #201f1f;
}

.container {
  width: 100%;
  padding: 0 15px;
  margin: 0 auto;

  @media screen and (min-width: 600px) {
    max-width: 480px;
    padding: 0;
  }
  @media screen and (min-width: 768px) {
    max-width: 600px;
  }
  @media screen and (min-width: 1200px) {
    width: 100%;
    padding: 0 15px;
  }
  @media screen and (min-width: 1440px) {
    max-width: 1320px;
    padding: 0;
  }
}
.section-title {
  font-size: 40px;
  font-weight: 300;
  line-height: 1.19;
  letter-spacing: -0.02em;
  text-transform: uppercase;
  margin-bottom: 50px;

  @media screen and (min-width: 1200px) {
    font-size: 90px;
    line-height: 1.06;
    margin-bottom: 80px;
  }
}
.section-padding {
  padding-top: 80px;

  @media screen and (min-width: 1200px) {
    padding-top: 200px;
  }
}
</style>
