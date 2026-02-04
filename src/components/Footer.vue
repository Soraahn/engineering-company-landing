<script setup>

</script>

<template>
  <footer class="footer">
      <div class="footer__main">
        <img src="#" alt="brand image" class="footer__brand">

        <address class="footer__contacts">
          <span class="footer__contacts-title">Contacts::</span>

          <div class="footer__contact-data">
            <p>
              Erwitter Str. 40<br>
              59590 Geseke<br>    
              GERMANY
            </p>
            
            <a href="tel:+492942978371"></a>
            <a href="mailto:info@m-bp.de">info@m-bp.de</a>
          </div>

          <nav class="footer__socials" aria-label="Social media">
            <span class="footer__socials-title">
              Our Social Media:
            </span>
            <a href="#" aria-label="Instagram">
              <img src="#" alt="Ig">
            </a>

            <a href="#" aria-label="Facebook">
              <img src="#" alt="Fb">
            </a>
          </nav>
        </address>

        <div class="footer__map">
          <iframe
            :src="'https://www.google.com/maps/embed?pb=!1m10!1m8!1m3!1d5958.890949578584!2d37.6095974545526' +
                  '!3d55.7722476417638!3m2!1i1024!2i768!4f13.1!5e0!3m2!1sru!2sde!4v1769330971463!5m2!1sru!2sde'"
            width="800"
            height="600"
            style="border:0;"
            allowfullscreen=""
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade">
          </iframe>
        </div>
      </div>

      <div class="footer__bottom">
        <div class="footer__legal">
          <a href="#" class="footer__imprint">Imprint</a>
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

</style>