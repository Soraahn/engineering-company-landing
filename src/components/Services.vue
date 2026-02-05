<script setup>
  const props = defineProps({
    firstServicesImage: {
      type: String,
      required: true,
    },
    secondServicesImage: {
      type: String,
      required: true,
    },
    servicesItems: {
      type: Array,
      required: true,
    },
  })
</script>

<template>
    <section class="services" id="services">
      <div class="services__intro">
        <h2 class="services__title">
          Comprehensive Structural Engineering Services
        </h2>
        <p class="services__description">
          We accompany you from the first idea of your next construction project from the first idea to successful 
          execution.
        </p>
      </div>
      <div class="services__viewport">
        <div class="services__list">
          <div
            v-for="item in servicesItems"
            :key="item.id"
            class="services__item"
            :data-area="item.gridArea"
            :data-type="item.type + '-block'"
          >
          <div class="services__item-viewport">
              <template
              v-if="item.type === 'text'">
                <div class="services__label">
                  <span
                    v-for="(line, i) in item.lines"
                    :key="i"
                    class="services__label-line"
                  >
                    {{ line }}
                  </span>
                </div>
            </template>
            <img
              v-else-if="item.type === 'image'"
              :src="item.src"
              alt=""
              aria-hidden="true"
              class="services__image"
            />  
          </div>
              
          </div>
        </div>
      </div>
      
      <div class="services__scroll-hint scroll-hint">
        <div class="scroll-hint__text">
          <span class="scroll-hint__text-line">Scroll to find out how our</span>
          <span class="scroll-hint__text-line">expertise can help you</span>
        </div>
      </div>
    </section>
</template>

<style scoped>
  .services {
    position: relative;
  }
  .services__intro   {
    margin-left: 287px;
    margin-top: 96px;
    max-width: fit-content;
    color: white;
    background-color: #06255B;
  }
  .services__title {
    max-width: 408px;
    font-weight: 700;
    font-style: bold;
    font-size: 40px;
    line-height: 100%;
    letter-spacing: -1px;
  }
  .services__description {
    max-width: 384px;
    margin-top: 24px;
    font-size: 18px;
    line-height: 130%;
    letter-spacing: 0.3px;
  }
  .services__viewport {
    overflow: hidden;
    margin-top: -360px;
    max-width: 1440px;
    transform: translateX(25px);
    padding: 246px 0 17px 0;
  }
  .services__list {
    display: grid;
    min-width: 0;
    grid-template-columns: repeat(6, 1fr);
    grid-template-rows: 1fr 1fr 1fr;
    grid-template-areas: 
    ". a . . . ."
    "b c d e f g"
    ". . . h . .";
    gap: 20px;
    color: black;
    
    transform: rotate(-45deg);
  }
  .services__item {
    width: 264px;
    height: 264px;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    font-weight: 700;
    font-size: 18px;
    letter-spacing: 0.3px;
    line-height: 100%;
  }
  .services__item[data-area="a"] {
    grid-area: a;
  }
  .services__item[data-area="b"] {
    grid-area: b;
  }
  .services__item[data-area="c"] {
    grid-area: c;
  }
  .services__item[data-area="d"] {
    grid-area: d;
  }
  .services__item[data-area="e"] {
    grid-area: e;
  }
  .services__item[data-area="f"] {
    grid-area: f;
  }
  .services__item[data-area="g"] {
    grid-area: g;
  }
  .services__item[data-area="h"] {
    grid-area: h;
  }
  .services__item-viewport {
    transform: rotate(45deg);
  }
  .services__item[data-type="text-block"] {
    background-color: white;
    box-shadow: inset 0 0 0 1px #D5D5D5;
  }
  .services__label {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
  .services__label-line {
    display: block;
    white-space: nowrap;
  }
  .services__label::after {
    content: '';
    display: block;
    width: 18px;
    height: 18px;
    margin-top: 15px;
    background: url('@/assets/services/svg/services_item_plus_icon.svg') center / contain no-repeat;
  }
  .services__item[data-area="g"] {
    transform: translateX(50px) translateY(0px);
  }
  .services__item[data-area="b"] {
    transform: translateX(0px) translateY(0px);
  }
  .services__scroll-hint {
    display: flex;
    justify-content: center;
    margin-top: 39px;
  }
  .scroll-hint__text {
    display: flex;
    flex-direction: column;
    align-items: center;
    font-weight: 600;
    font-size: 18px;
    line-height: 120%;
    letter-spacing: 0.26px;
    color: #53565A;
  }
  @keyframes scrollHint {
    0% { transform: translateY(0); }
    50% { transform: translateY(6px); }
    100% { transform: translateY(0); }
  }
  .scroll-hint__text::after {
    content: '';
    display: block;
    width: 30px;
    height: 32px;
    margin: 20px auto 0;
    
    animation: scrollHint 2s ease-in-out infinite;

    background: url('@/assets/services/svg/scroll_hint_icon.svg') center / contain no-repeat;
  }
</style>