<script setup>
    const props = defineProps ({
        expertiseAreas: {
            type: Array,
            required: true,
        },
    })
</script>

<template>
  <section class="expertise" id="projects-and-references">
      <header class="expertise__intro">
        <div class="expertise__intro-container">
          <h2 class="expertise__title">
            Broad expertise based on decades of experience
          </h2>
          <p class="expertise__description">
            Our services include all types of construction projects that you encounter.
          </p>
        </div>
      </header>

      <div class="expertise__areas">
        <div
          v-for="area in expertiseAreas"
          :key="area.id"
          class="expertise__area"
        >
          <span class="expertise__area-index">
            {{ area.id }}
          </span>
          <span class="expertise__area-text">
            {{ area.text }}
          </span>
        </div>
      </div>
    </section>
</template>

<style scoped>
.expertise {
    margin-top: 152px;
  }
  .expertise__intro {
    display: flex;
    justify-content: center;
  }
  .expertise__intro-container {
    display: flex;
    width: 536px;
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
  .expertise__title {
    color: black;
    font-weight: 700;
    font-style: Bold;
    font-size: 40px;
    line-height: 100%;
    letter-spacing: -1px;
  }
  .expertise__description {
    margin-top: 24px;
    font-weight: 400;
    font-size: 18px;
    line-height: 130%;
    letter-spacing: 0.3px;
    color: #737B7D;
  }
  .expertise__areas {
    margin-top: 51px;
    height: 488px;
    position: relative;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr;
    overflow: hidden;
    cursor: pointer;
  }
  .expertise__areas::before {
    content: "";
    position: absolute;
    inset: 0;
    z-index: 0;

    background: url("@/assets/expertise/svg/expertise-areas-background.svg") no-repeat;
    background-size: 100% 100%;
    background-position: bottom center;
    pointer-events: none;
  }
  .expertise__area {
    padding: 55px 37px;
    position: relative;
    border: solid 1px #E2E2E2;
  }
  .expertise__area * {
    position: relative;
    z-index: 1;
    transition: 0.3s ease;
  }
  .expertise__area::before {
    content: '';
    position: absolute;
    display: block;
    inset: 0;
    background: url('@/assets/expertise/png/area-background_hover.png') no-repeat;
    background-size: auto 100%;
    background-position: 55% center;
    opacity: 0;
    transition: 0.3s ease;
  }
  .expertise__area:hover::before {
    opacity: 1;
  }
  .expertise__area-index {
    display: block;
    font-family: Mulish;
    font-weight: 800;
    font-size: 17px;
    line-height: 100%;
    letter-spacing: 0.3px;
    color: #DA5D24;
  }
  .expertise__area-index::before,
  .expertise__area-index::after {
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    width: 25px;
    height: 25px;
    transform: translateX(16px) translateY(13px);
    transition: 0.3s ease;
  }
  .expertise__area-index::after {
    opacity: 1;
    background: url('@/assets/expertise/svg/area-index-icon-centered.svg') no-repeat;
  }
  .expertise__area-index::before {
    opacity: 0;
    background: url('@/assets/expertise/svg/area-index-icon-hover-centered.svg') no-repeat;
  }
  .expertise__area:hover .expertise__area-index::after {
    opacity: 0;
  }
  .expertise__area:hover .expertise__area-index::before {
    opacity: 1;
  }
  .expertise__area:hover .expertise__area-index{
    color: white;
    text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  }
  .expertise__area:hover .expertise__area-index::after {
    background: url('@/assets/expertise/svg/area-index-icon-hover-centered.svg') no-repeat;
  }
  .expertise__area-text {
    display: block;
    margin-top: 180px;
    font-family: Mulish;
    font-weight: 800;
    font-size: 17px;
    line-height: 100%;
    letter-spacing: 0.3px;
    color: #2F3034;
  }
  .expertise__area:hover .expertise__area-text {
    color: white;
    text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  }
</style>