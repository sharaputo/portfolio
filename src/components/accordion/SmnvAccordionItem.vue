<template>
  <li class="accordion__item">
    <div class="accordion__trigger" :class="{ _active: visible }" @click="open">
      <slot name="accordion-trigger"></slot>
      <span class="btn">
        <svg
          width="17"
          height="17"
          viewBox="0 0 17 17"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M7.75871 0H9.24127C9.37305 0 9.43894 0.062963 9.43894 0.188889V16.8111C9.43894 16.937 9.37305 17 9.24127 17H7.75871C7.62693 17 7.56104 16.937 7.56104 16.8111V0.188889C7.56104 0.062963 7.62693 0 7.75871 0Z"
          />
          <path
            d="M0.197674 7.60254H16.8023C16.9341 7.60254 17 7.6655 17 7.79143V9.20809C17 9.33402 16.9341 9.39698 16.8023 9.39698H0.197674C0.0658915 9.39698 0 9.33402 0 9.20809V7.79143C0 7.6655 0.0658915 7.60254 0.197674 7.60254Z"
          />
        </svg>
      </span>
    </div>

    <transition
      name="accordion"
      @enter="start"
      @after-enter="end"
      @before-leave="start"
      @after-leave="end"
    >
      <div class="accordion__content" v-show="visible">
        <slot name="accordion-content"></slot>
      </div>
    </transition>
  </li>
</template>

<script>
export default {
  inject: ["Accordion"],
  data() {
    return {
      index: null,
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
.accordion {
  &__item {
    position: relative;
    padding: 15px 0;
    border-top: 1px solid #a1a1a1;
    -webkit-tap-highlight-color: transparent;
    cursor: pointer;

    &:last-child {
      border-bottom: 1px solid #a1a1a1;
    }

    @media screen and (min-width: 1200px) {
      padding: 20px 0;
    }
  }
  &__trigger {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;

    .btn {
      display: grid;
      place-items: center;
      flex-shrink: 0;
      width: 27px;
      height: 27px;
      border-radius: 50%;
      transition: background-color 0.3s ease-in-out, transform 0.3s ease-in-out;

      svg {
        fill: #fff;
        transition: fill 0.3s ease-in-out;
      }
    }
    &._active .btn {
      background-color: #fff;
      transform: rotate(45deg);

      svg {
        fill: #201f1f;
      }
    }

    &:hover:not(._active) .btn svg {
      fill: #a1a1a1;
    }
  }

  h3 {
    font-size: 20px;
    font-weight: 400;
    text-transform: uppercase;

    @media screen and (min-width: 1200px) {
      font-size: 30px;
    }
  }
  p {
    font-size: 15px;
    color: #a1a1a1;
    padding: 25px 0 10px;

    @media screen and (min-width: 1200px) {
      font-size: 16px;
      padding: 15px 0 0;
    }
  }

  @media screen and (min-width: 1200px) {
    max-width: 872px;
    margin-left: auto;
  }
}
.accordion-enter-active,
.accordion-leave-active {
  will-change: height, opacity;
  transition: height 0.3s ease, opacity 0.3s ease;
  overflow: hidden;
}
.accordion-enter-from,
.accordion-leave-to {
  height: 0 !important;
  opacity: 0;
}
</style>
