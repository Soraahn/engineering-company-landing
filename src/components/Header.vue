<script setup>
  const props = defineProps({
    navLinks: {
      type: Array,
      required: true,
    },
    currentLang: {
      type: String,
      required: true,
    },
  })

  const emit = defineEmits(['change-lang'])

  function onLangClick(lang) {
    emit('change-lang', lang)
  }
</script>

<template>
  <header class="header">
      <nav class="header__navigation-bar navigation-bar">
        <img src="@/assets/header/svg/logo.svg" alt="logo" class="header__logo">
        <div class="navigation-bar__links">
          <a
            v-for="link in navLinks"
            :key="link.id"
            :href="link.href"
            :class="link.class"
            class="navigation-bar__link link"
          >
            {{ link.label }}
          </a>
          
        </div>
        <div class="navigation-bar__actions">
          <a class="navigation-bar__contact-us-btn btn contact-us-btn" href="#">
            Contact Us
          </a>
          <div class="navigation-bar__change-lang-buttons">
            <button
              @click="onLangClick('de')"
              class="navigation-bar__German-lang-btn navigation-bar__change-lang-button"
              data-active="false"
            ><span>De.</span></button>
            <button
              @click="onLangClick('en')"
              class="navigation-bar__English-lang-btn navigation-bar__change-lang-button"
              data-active="true"
            ><span>En.</span></button>
            <button
              @click="onLangClick('fr')"
              class="navigation-bar__French-lang-btn navigation-bar__change-lang-button"
              data-active="false"
            ><span>Fr.</span></button>
          </div>
        </div>
        
      </nav>
      <div class="hero">
        <div class="container">
          <h1 class="hero__title">
            Civil <span class="hero__emphasis">Engineering Solutions</span>
          </h1>
          <p class="hero__subtitle">
            For The <span class="hero__emphasis">Cement</span> Industry
          </p>
        </div>
        <div class="hero__text">
          <p class="hero__text-item">
            We are your leading partner for complex brownfield construction projects during ongoing operation.
          </p>
          <p class="hero__text-item">
            Benefit from engineering excellence built on more than 30 years of industry experience.
          </p>
        </div>
        <div class="hero__actions">
          <a href="#" class="hero__button hero__button--secondary">
            How can we serve you
          </a>
          <a href="#" class="hero__button hero__button--primary">
            Contact Us
          </a>
        </div>
      </div>
    </header>
</template>

<style scoped>
  .header {
    position: relative;
    overflow: hidden;
    height: 1024px;
    color: white;
    background:
      linear-gradient(to right, rgba(6, 37, 91, 1) 0%, rgba(6, 37, 91, 0) 60%),
      linear-gradient(to bottom, rgba(6, 37, 91, 1) 0%, rgba(6, 37, 91, 0) 40%),
      url("@/assets/header/jpg/background.jpg") center / cover no-repeat;
  }
  .header::before {
    content: '';
    position: absolute;
    right: 30px;
    top: 200px;
    width: 500px;
    height: 500px;
    background: url("@/assets/header/svg/Group 1201.svg") no-repeat;
    background-size: auto;
  }
  .header::after {
    content: '';
    position: absolute;
    right: 0;
    top: 34px;
    width: 1000px;
    height: 1000px;
    background: url("@/assets/header/svg/Group 2348.svg")no-repeat;
    background-position: right top;
    background-size: auto;
    z-index: 100;
  }
  .header__logo {
    margin-top: 37px;
    margin-left: 87px;
    height: 46px;
  }

  .navigation-bar {
    display: flex;
    justify-content: space-between;
  }

  .navigation-bar__links {
    height: fit-content;
    margin-top: 65px;
    display: flex;
    gap: 32px;
  }
  .navigation-bar__links a {
    font-weight: 400;
    font-size: 15px;
    line-height: 18px;
    letter-spacing: 0.2px;
    vertical-align: middle;
    transition: color 0.2s linear;

  }
  .navigation-bar__links a:hover {
    color: #BA4E1D;
  }

  .navigation-bar__actions {
    margin-top: 48px;
    height: 56px;
    display: flex;
    gap: 16px;
  }
  .contact-us-btn {
    width: 143px;
    height: 56px;
    color: white;
    background-color: #DA5D24;
    display: inline-flex;
    justify-content: center;
    align-items: center;
    font-weight: 600;
    transition: background-color 0.2s linear;
  }
  .contact-us-btn:hover {
    background-color: #BA4E1D;
  }
  .navigation-bar__change-lang-buttons {
    padding: 18px 19px 20px 15px;
    background-color: white;
    display: flex;
    align-items: center;
    gap: 12px;
    color: #06255B;
  }
  .navigation-bar__change-lang-button span {
    opacity: 40%;
    transition: all 0.2s linear;
  }
  .navigation-bar__change-lang-button:hover span {
    opacity: 100%;
    text-decoration: underline;
    text-decoration-thickness: 1px;
    text-underline-offset: 4px;
  }
  .navigation-bar__change-lang-button[data-active="true"] span {
    opacity: 100%;
    
  }
  .navigation-bar__change-lang-button::before {
    content: '';
    display: inline-block;
    width: 12px;
    height: 12px;
    margin-right: 6px;
  }
  .navigation-bar__German-lang-btn::before {
    background: url('@/assets/header/svg/german_lang_icon.svg') center / cover no-repeat;
  }
  .navigation-bar__English-lang-btn::before {
    background: url('@/assets/header/svg/english_lang_icon.svg') center / cover no-repeat;
  }
  .navigation-bar__French-lang-btn::before {
    background: url('@/assets/header/svg/french_lang_icon.svg') center / cover no-repeat;
  }

  .hero {
    margin-left: 166px;
    margin-top: 196px;
  }
  .hero::before {
    content: '';
    position: absolute;
    right: 210px;
    top: 402px;
    width: 500px;
    height: 500px;
    background: url("@/assets/header/svg/Group 1200.svg") no-repeat;
    background-size: auto;
  }
  .hero::after {
    content: '';
    position: absolute;
    right: 49px;
    top: 520px;
    width: 500px;
    height: 500px;
    background: url("@/assets/header/svg/Group 1202.svg") no-repeat;
    background-size: auto;
  }
  .hero__title, .hero__subtitle {
    font-weight: 400;
    font-size: 64px;
    line-height: 110.00000000000001%;
    letter-spacing: -1.47px;
  }
  .hero__emphasis {
    font-weight: 700;
    font-style: bold;
  }
  .hero__text {
    margin-top: 24px;
    display: flex;
    flex-direction: column;
    gap: 28px;
    
    font-size: 25px;
    line-height: 110.00000000000001%;
  }
  .hero__text-item:first-child {
    max-width: 623px;
  }
  .hero__text-item:last-child {
    max-width: 489px;
  }

  .hero__actions {
    margin-top: 40px;
    display: flex;
    gap: 16px;
  }
  .hero__button {
    font-weight: 600;
    font-size: 15px;
    line-height: 18px;
    letter-spacing: 0.3px;
    display: flex;
    justify-content: center;
    align-items: center;
    transition: all 0.3s linear;
  }
  .hero__button--primary {
    width: 133px;
    height: 51px;
    display: flex;
    background: white;
    color: #06255B;
  }
  .hero__button--primary:hover {
    background-color: #ABB5C7;
    color: white;
  }
  .hero__button--secondary {
    width: 194px;
    height: 51px;
    box-shadow: inset 0 0 0 2px white;
    background-color: #06255B99;
  }
  .hero__button--secondary:hover {
    background-color: white;
    color: #06255B;
  }
</style>