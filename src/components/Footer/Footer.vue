<script setup>
  import Map from "@/components/Footer/Map.vue";
</script>

<template>
  <footer class="footer">
      <div class="footer__map">
        <Map />

        <div class="footer__main">
          <img class="footer__brand" src="@/assets/footer/footer__brand.svg" alt="brand image">

          <address class="footer__contacts">
            <span class="footer__contacts-title">Contacts::</span>

            <div class="footer__contact-data">
              <p class="footer__contact-adress">
                Erwitter Str. 40<br>
                59590 Geseke<br>    
                GERMANY
              </p>
              
              <a class="footer__contact-tel" href="tel:+492942978371">+49 29 42 / 97 83 71</a>
              <a class="footer__contact-mail" href="mailto:info@m-bp.de">info@m-bp.de</a>
            </div>

            <nav class="footer__socials" aria-label="Social media">
              <span class="footer__socials-title">
                Our Social Media:
              </span>
              <div class="footer__socials-links">
                <a href="#" aria-label="Instagram">
                  <img src="@/assets/footer/Instagram.svg" alt="Ig">
                </a>

                <a href="#" aria-label="Facebook">
                  <img src="@/assets/footer/facebook.svg" alt="Fb">
                </a>
              </div>
            </nav>
          </address>
        </div>
      </div>

      <div class="footer__bottom">
        <div class="footer__legal">
          <a href="#" class="footer__imprint">Imprint</a>
          <span>|</span>
          <a href="#" class="footer__data-privacy">Data Privacy</a>
        </div>

        <div class="footer__copyright">
          Copyright : mbp | Mollenhauer Beraten & Planen GmbH
        </div>

        <div class="footer__tagline">
          Consulting & Structural Engineering Design
        </div>
      </div>
    </footer>
</template>

<style scoped>
  .footer {
    margin-top: 80px;
  }
  .footer::before {
    content: "";
    display: block;
    margin-bottom: 4px;
    width: 156px;
    height: 143px;
    background: url("@/assets/footer/Rectangle 163.svg") no-repeat ;
  }
  .footer__map {
    height: 400px;
    overflow: hidden;
    position: relative;
  }
  .footer__main {
    margin-left: 2px;
    width: 493px;
    height: 346px;
    box-sizing: border-box;
    padding: 24px 0 0 73px;
    display: flex;

    position: absolute;
    z-index: 1;
    top: 50%;
    transform: translateY(-50%);

    background-color: white;
  }
  .footer__brand {
    width: 72px;
    height: 55px;
  }
  .footer__contacts {
    margin-left: 69px;
    margin-top: 23px;

    font-style: normal;
    color: #313131;
  }
  .footer__contacts-title {
    font-weight: 700;
    font-size: 15px;
    line-height: 22px;
    letter-spacing: 0%;
  }
  .footer__contact-data {
    margin-top: 27px;

    display: flex;
    flex-direction: column;
    gap: 16px;

    font-family: Roboto;
    font-weight: 400;
    font-size: 15px;
    line-height: 150%;
    letter-spacing: 0%;
  }
  .footer__contact-mail {
    display: inline-block;
    color: #FF7C40;
  }
  .footer__socials {
    margin-top: 28px;
    display: flex;
    align-items: center;
    gap: 28px;
  }
  .footer__socials-title {
    font-family: Source Sans Pro;
    font-weight: 700;
    font-size: 15px;
    line-height: 22px;
    letter-spacing: 0%;
    color: #313131;
  }
  .footer__socials-links {
    display: flex;
    align-items: center;
    gap: 16px;
  }
  .footer__socials-links a {
    line-height: 0;
  }
  .footer__bottom {
    height: 80px;
    padding: 0 144px 0 144px;

    display: flex;
    justify-content: space-between ;
    align-items: center;

    background-color: #06255B;

    font-family: Source Sans Pro;
    font-weight: 300;
    font-size: 14px;
    line-height: 22px;
    letter-spacing: 0.3px;
    color: white;

  }
  .footer__legal {
    display: flex;
    gap: 10px;
  }
  .footer__copyright {
    margin-left: 200px;
  }
</style>