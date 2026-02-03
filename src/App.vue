<script setup>
  const navLinks = [
    {label: "Services", href: "#services", class: "navigation-bar__services", id: crypto.randomUUID()},
    {label: "Know How", href: "#know-how", class: "navigation-bar__know-how", id: crypto.randomUUID()},
    {label: "Projects & References", href: "#projects-and-references", class: "navigation-bar__projects-and-references", id: crypto.randomUUID()},
    {label: "Our Company", href: "#our-company", class: "navigation-bar__our-company", id: crypto.randomUUID()},
    {label: "Our Clients", href: "#our-clients", class: "navigation-bar__our-clients", id: crypto.randomUUID()},
    {label: "Careers", href: "#careers", class: "navigation-bar__careers", id: crypto.randomUUID()},
  ];

  import {ref} from 'vue';
  const currentLang = ref('en');
  
  function setLanguage(lang) {
    currentLang.value = lang;
  }
  import first_services_image from '@/assets/services/svg/image 85 (1).svg';
  import second_services_image from '@/assets/services/svg/image_85.svg';

  const servicesItems = [
    {
      id: crypto.randomUUID(),
      type: 'text',
      lines: [
        'Project consulting',
      ],
      gridArea: 'a'
    },
    {
      id: crypto.randomUUID(),
      type: 'image',
      src: first_services_image,
      gridArea: 'b'
    },
    {
      id: crypto.randomUUID(),
      type: 'text',
      lines: [
        'Location analysis and',
        'feasibility studies',
      ],
      gridArea: 'c'
    },
    {
      id: crypto.randomUUID(),
      type: 'text',
      lines: [
        'Structural design and',
        'execution planning',
      ],
      gridArea: 'd'
    },
    {
      id: crypto.randomUUID(),
      type: 'text',
      lines: [
        'Preparation of contract',
        'award'
      ],
      gridArea: 'e'
    },
    {
      id: crypto.randomUUID(),
      type: 'text',
      lines: [
        'Service and',
        'Support',
      ],
      gridArea: 'f'
    },
    {
      id: crypto.randomUUID(),
      type: 'image',
      src: second_services_image,
      gridArea: 'g'
    },
    {
      id: crypto.randomUUID(),
      type: 'text',
      lines: [
        'Construction site',
        'consulting',
      ],
      gridArea: 'h'
    },
  ];

  const expertiseAreas = [
    {
      id: '1',
      text: 'Civil engineering'
    },
    {
      id: '2',
      text: 'Machine and building foundations'
    },
    {
      id: '3',
      text: 'Silo and slipform construction'
    },
    {
      id: '4',
      text: 'Assesments, building inspection, concrete maintenance and repair'
    },
    {
      id: '5',
      text: 'International cement factory construction'
    },
    {
      id: '6',
      text: 'Construction in ongoing operations'
    },
  ];

  const testimonials = [
    {
      id: 1,
      logo: '#',
      alt: 'thomas gruppe logo',
      text: "“Pulvinar nisl nulla elit integer diam maecenas. Mauris nunc at arcu urna. Erat quisque neque, a augue " +
            "lectus vitae faucibus facilisi. Aenean mauris duis sed congue magna scelerisque dolor eget in. Euismod " +
            "eros, in cursus aliquam. Suspendisse odio est nullam vulputate quis nam ultricies.”",
      author: {
        name: 'Jack Carty',
        position: 'SEO'
      }
    },
    {
      id: 2,
      logo: '#',
      alt: 'zl logo',
      text: "“Pulvinar nisl nulla elit integer diam maecenas. Mauris nunc at arcu urna. Erat quisque neque, a augue " +
            "lectus vitae faucibus facilisi. Aenean mauris duis sed congue magna scelerisque dolor eget in. Euismod " +
            "eros, in cursus aliquam. Suspendisse odio est nullam vulputate quis nam ultricies.”",
      author: {
        name: 'Jack Carty',
        position: 'SEO'
      }
    },
    {
      id: 3,
      logo: '#',
      alt: 'Buzzi Unicem logo',
      text: "“Pulvinar nisl nulla elit integer diam maecenas. Mauris nunc at arcu urna. Erat quisque neque, a augue " +
            "lectus vitae faucibus facilisi. Aenean mauris duis sed congue magna scelerisque dolor eget in. Euismod " +
            "eros, in cursus aliquam. Suspendisse odio est nullam vulputate quis nam ultricies.”",
      author: {
        name: 'Jack Carty',
        position: 'SEO'
      }
    },
    {
      id: 4,
      logo: '#',
      alt: 'thomas gruppe logo',
      text: "“Pulvinar nisl nulla elit integer diam maecenas. Mauris nunc at arcu urna. Erat quisque neque, a augue " +
            "lectus vitae faucibus facilisi. Aenean mauris duis sed congue magna scelerisque dolor eget in. Euismod " +
            "eros, in cursus aliquam. Suspendisse odio est nullam vulputate quis nam ultricies.”",
      author: {
        name: 'Jack Carty',
        position: 'SEO'
      }
    },
    {
      id: 5,
      logo: '#',
      alt: 'cemex logo',
      text: "“Pulvinar nisl nulla elit integer diam maecenas. Mauris nunc at arcu urna. Erat quisque neque, a augue " +
            "lectus vitae faucibus facilisi. Aenean mauris duis sed congue magna scelerisque dolor eget in. Euismod " +
            "eros, in cursus aliquam. Suspendisse odio est nullam vulputate quis nam ultricies.”",
      author: {
        name: 'Jack Carty',
        position: 'SEO'
      }
    },
  ];

  const activeIndex = ref(0);

  const groups = [
    {
      id: 1,
      class: 'engineers',
      title: 'Engineers',
      members: [
        {
          id: crypto.randomUUID(),
          avatar: '#',
          name: 'Bernhard Meyer',
          position: 'Senior Steel Structures Engineer'
        },
        { 
          id: crypto.randomUUID(),
          avatar: '#',
          name: 'Alexander Jung',
          position: 'Project Engineer'
        },
        {
          id: crypto.randomUUID(),
          avatar: '#',
          name: 'Stefan Schniedermeier',
          position: 'Project Engineer'
        },
        {
          id: crypto.randomUUID(),
          avatar: '#',
          name: 'Stefan Wiek',
          position: 'Project Engineer'
        },
        {
          id: crypto.randomUUID(),
          avatar: '#',
          name: 'You?',
          cta: {
            label: 'Apply Now',
            link: '#'
          },
          position: 'Senior Engineer Concrete'
        },
      ]
    },
    {
      id: 2,
      class: 'technical-staff',
      title: 'Technical staff',
      members: [
        {
          id: crypto.randomUUID(),
          avatar: '#',
          name: 'Domenik Schmidt',
          position: 'Head of Layout & Design'
        },
        {
          id: crypto.randomUUID(),
          avatar: '#',
          name: 'Manuela Sonntag',
          position: 'Reinforcement TechnicianHead of Layout & Design'
        },
        {
          id: crypto.randomUUID(),
          avatar: '#',
          name: 'Mark Peters',
          position: 'Planning Permission Design'
        },
        {
          id: crypto.randomUUID(),
          avatar: '#',
          name: 'Katarina Maslanova',
          position: 'Structural Drawings'
        },
        {
          id: crypto.randomUUID(),
          avatar: '#',
          name: 'Benedikt Schröder-Schlüter',
          position: 'Structural Drawings'
        },
        {
          id: crypto.randomUUID(),
          avatar: '#',
          name: 'Michael Dick',
          position: 'Structural Drawings'
        },
      ]
    },
    {
      id: 3,
      class: 'engineering-trainees',
      title: 'Engineering Trainees',
      members: [
        {
          id: crypto.randomUUID(),
          avatar: '#',
          name: 'Najwa Hasan',
          position: 'Position'
        },
        {
          id: crypto.randomUUID(),
          avatar: '#',
          name: 'Leonie Kahr',
          position: 'Position'
        },
      ]
    },
    {
      id: 4,
      class: 'other-members',
      title: 'Other Team Members',
      members: [
        {
          id: crypto.randomUUID(),
          avatar: '#',
          name: 'Michelle Michalik',
          position: 'Assistent to the Management'
        }
      ]
    }
  ];
  
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
            @click="setLanguage('de')"
            class="navigation-bar__German-lang-btn navigation-bar__change-lang-button"
            data-active="false"
          ><span>De.</span></button>
          <button
            @click="setLanguage('en')"
            class="navigation-bar__English-lang-btn navigation-bar__change-lang-button"
            data-active="true"
          ><span>En.</span></button>
          <button
            @click="setLanguage('fr')"
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

  <section class="services" id="services">
    <div class="services__intro">
      <h2 class="services__title">
        Comprehensive Structural Engineering Services
      </h2>
      <p class="services__description">
        We accompany you from the first idea of your next construction project from the first idea to successful execution.
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

    <div class="expertise__lifecycle" id="know-how">
      <header class="expertise__lifecycle-header">
        <h2 class="expertise__lifecycle-title">
          Benefit from Decades of Life Cycle Know How
        </h2>
        <p class="expertise__lifecycle-description">
          Our decade-long permanent presence on cement plants helps us to design buildings today that will be ready for 
          whatever tomorrow brings. With our comprehensive planning methodology and building life cycle experience we 
          anticipate use changes, unexpected utilisation and lifetime expositions early on during planning. 
          This allows us to design buildings that are flexible, long-lasting, and economically efficient.
        </p>
      </header>

      <div class="expertise__lifecycle-slider step-slider">
        <div class="step-slider__steps">
          <button class="step-slider__step">
            <span class="step-slider__step-index">01</span>
            <span class="step-slider__step-description">
              Comprehensive planning methodology includes life-cycle know how
            </span>
          </button>

          <button class="step-slider__step is-active">
            <span class="step-slider__step-index">02</span>
            <span class="step-slider__step-description">
              Greenfield. Brownfield. Ongoing Operation.
            </span>
          </button>

          <button class="step-slider__step">
            <span class="step-slider__step-index">03</span>
            <span class="step-slider__step-description">
              Reuse, rebuild, extend
            </span>
          </button>

          <button class="step-slider__step">
            <span class="step-slider__step-index">04</span>
            <span class="step-slider__step-description">
              Renovate, refurbish, revamp
            </span>
          </button>

          <button class="step-slider__step">
            <span class="step-slider__step-index">05</span>
            <span class="step-slider__step-description">
              Demolition
            </span>
          </button>
        </div>

        <div class="step-slider__stage">
          <div class="step-slider__controls">
            <button class="step-slider__control step-slider__control--prev"></button>
            <button class="step-slider__control step-slider__control--next"></button>
          </div>
          <div class="step-slider__media">
            <img src="#" alt="">
          </div>
          <div class="step-slider__content">
            <h3 class="step-slider__title">
              Comprehensive planning methodology includes life-cycle know how
            </h3>
            <p class="step-slider__text">
              Our decade-long permanent presence on cement plants allows us to anticipate use changes, unexpected 
              utilisation and lifetime expositions early on during planning. This allows us to design buildings that 
              are flexible, long-lasting and economically efficient.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
  
  <section class="trust" id="our-clients">
    <div class="trust__logos logo-slider">
        <h2 class="logo-slider__title">
          Key Players in the cement industry trust us.
        </h2>

        <div class="logo-slider__viewport">
          <button class="logo-slider__control logo-slider__control--prev"></button>

          <ul class="logo-slider__track">
            <li class="logo-slider__item">
              <img src="#" alt="" class="logo-slider__item-logo">
            </li>
            <li class="logo-slider__item">
              <img src="#" alt="" class="logo-slider__item-logo">
            </li>
            <li class="logo-slider__item">
              <img src="#" alt="" class="logo-slider__item-logo">
            </li>
            <li class="logo-slider__item">
              <img src="#" alt="" class="logo-slider__item-logo">
            </li>
            <li class="logo-slider__item">
              <img src="#" alt="" class="logo-slider__item-logo">
            </li>
            <li class="logo-slider__item">
              <img src="#" alt="" class="logo-slider__item-logo">
            </li>
            <li class="logo-slider__item">
              <img src="#" alt="" class="logo-slider__item-logo">
            </li>
            <li class="logo-slider__item">
              <img src="#" alt="" class="logo-slider__item-logo">
            </li>
            <li class="logo-slider__item">
              <img src="#" alt="" class="logo-slider__item-logo">
            </li>
            <li class="logo-slider__item">
              <img src="#" alt="" class="logo-slider__item-logo">
            </li>
            <li class="logo-slider__item">
              <img src="#" alt="" class="logo-slider__item-logo">
            </li>
            <li class="logo-slider__item">
              <img src="#" alt="" class="logo-slider__item-logo">
            </li>
            <li class="logo-slider__item">
              <img src="#" alt="" class="logo-slider__item-logo">
            </li>
            <li class="logo-slider__item">
              <img src="#" alt="" class="logo-slider__item-logo">
            </li>
            <li class="logo-slider__item">
              <img src="#" alt="" class="logo-slider__item-logo">
            </li>
          </ul>

          <button class="logo-slider__control logo-slider__control--next"></button>
        </div>
      </div>

      <div class="trust__testimonials testimonial-slider">
        <header class="testimonial-slider__intro">
          <h3 class="testimonial-slider__title">
            What clients say.
          </h3>
          <p class="testimonial-slider__description">
            Aenean mauris duis sed congue magna scelerisque dolor eget in. Euismod eros, in cursus aliquam.
          </p>
        </header>

        <div class="testimonial-slider__pagination">
          <button class="testimonial-slider__dot testimonial-slider__dot--active"></button>
          <button class="testimonial-slider__dot"></button>
          <button class="testimonial-slider__dot"></button>
          <button class="testimonial-slider__dot"></button>
          <button class="testimonial-slider__dot"></button>
        </div>

        <div class="testimonial-slider__stage">
          <article
            v-for="(testimonial, index) in testimonials"
            :key="testimonial.id"
            class="testimonial-slider__slide"
            :class="{'testimonial-slider__slide--active' : index === activeIndex}" 
          >
            <div class="testimonial-slider__logo">
              <img
                :src="testimonial.logo"
                :alt="testimonial.alt"
              />
            </div>

            <blockquote class="testimonial-slider__text">
              {{ testimonial.text }}
            </blockquote>

            <div class="testimonial-slider__author">
              <span class="testimonial-slider__name">
                {{ testimonial.author.name }}
              </span>
              <span class="testimonial-slider__position">
                {{ testimonial.author.position }}
              </span>
            </div>
          </article>
        </div>

        <div class="testimonial-slider__controls">
          <button class="testimonial-slider__control testimonial-slider__control--prev"></button>
          <button class="testimonial-slider__control testimonial-slider__control--next"></button>
        </div>
      </div>

  </section>
  
  <section class="about" id="our-company">
    <div class="about__values">
      <header class="about__values-intro">
        <span class="about__values-eyebrow">
          Holistic. Agile. Reliable
        </span>

        <h2 class="about__values-title">
          With this triad we line up to support you to realize your projects successfully. 
        </h2>

        <div class="about__values-description">
          <p>
            Today’s construction projects are notable for the diversity of their requirements. While you want your 
            buildings to be safe, economical, and durable, they primarily serve your operations. Our deep industry 
            knowledge helps to optimally incorporate the variety of usage requirements of the cement production processes 
            into civil design.
          </p>
          <p>
            We constantly achieve client success by following these three core values for all projects our clients 
            trust us with.
          </p>
        </div>

      </header>

      <ul class="about__values-list">
        <li class="about__value">
          <h3 class="about__value-title">
            Holistic planning
          </h3>
          <p class="about__value-description">
            Through continuous consideration of all circumstances, we create futureproof buildings and frictionless 
            construction workflows. Systematic implementation of this holistic approach helps us to keep the bird’s-eye 
            view over all interfaces. We are proactively making sure that all included parties can focus on working 
            towards the optimal project result.
          </p>
        </li>
        
        <li class="about__value">
          <h3 class="about__value-title">
            Agile acting
          </h3>
          <p class="about__value-description">
            Our team can put results down on paper rapidly. In a world that is increasingly characterized by changing 
            and adapting to uncertain circumstances, we can flexibly execute on multiple iterations of the project in 
            close consultation with the client. This allows us to cater to your construction needs until the last 
            phases of planning.
          </p>
        </li>

        <li class="about__value">
          <h3 class="about__value-title">
            Reliable realisation.
          </h3>
          <p class="about__value-description">
            We prioritize project success over everything. Based on our decades of experience we have developed the 
            highest quality standards and demonstrate with every new project our commitment to meeting and exceeding 
            client expectations. 
          </p>
        </li>
      </ul>
    </div>

    <div class="about__team" id="careers">
      <header class="about__team-intro">
        <h2 class="about__team-title">
          Meet the Team
        </h2>
        <p class="about__team-subtitle">
          These are the experts that turn ideas into reality
        </p>
      </header>

      <section class="about__team-group about__team-group--leadership">
        <h3 class="about__team-title">
          Leadership Team
        </h3>
        <ul class="about__team-list team">
          <li class="team__member">
            <img src="#" alt="" class="team__member-avatar">
            <h4 class="team__member-name">
              Tim-Nicolas Mollenhauer
            </h4>
            <span class="team__member-position">
              CEO
            </span>
            <p class="team__member-bio">
              Viverra in turpis vitae tincidunt. Odio nunc netus consectetur libero duis. Est quis vitae, sed egestas 
              vehicula.
            </p>
            <a href="#" class="team__member-linked-in"></a>
          </li>

          <li class="team__member">
            <img src="#" alt="" class="team__member-avatar">
            <h4 class="team__member-name">
              Klaus-Dieter Mollenhauer
            </h4>
            <span class="team__member-position">
              Creative Director
            </span>
            <p class="team__member-bio">
              Duis aenean ultricies ullamcorper neque cras vel. Quam sem turpis est morbi nunc odio feugiat 
              pellentesque. Eget risus lectus donec tempus cras. Amet amet, auctor habitasse tristique pellentesque 
              id velit.
            </p>
            <a href="#" class="team__member-linked-in"></a>
          </li>
        </ul>

      </section>

      <section 
        v-for="group in groups"
        :key="group.id"
        class="about__team-group"
        :class="'about__team-' + group.class"
      >
        <h3 class="about__team-title">
          {{ group.title }}
        </h3>

        <ul class="about__team-list team">
          <li
            v-for="member in group.members"
            :key="member.id"
            class="team__member"
          >
            <img
              :src="member.avatar"
              alt=""
              aria-hidden="true"
              class="team__member-avatar"
            />
            <h4 class="team__member-name">
              {{ member.name }}
            </h4>
            <a v-if="member.cta" class="team__member-apply-button" :href="member.cta.link">{{ member.cta.label }}</a>
            <span class="team__member-position">
              {{ member.position }}
            </span>
          </li>
        </ul>
      </section>
    </div>
  </section>

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
  body {
    font-family: 'Source Sans Pro';
  }
  a {
    text-decoration: none;
    color: inherit;
  }
  button {
    all: unset;
    cursor: pointer;
  }

  .header {
    height: 1223px;
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

  .services__intro   {
    margin-left: 287px;
    margin-top: 96px;
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
    transform: translateX(50px) translateY(-180px);
  }
  .services__list {
    display: grid;
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
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr;
  }
  .expertise__area {
    padding: 55px 37px;
    border: solid 1px red;
  }
  .expertise__area-index {
    font-family: Mulish;
    font-weight: 800;
    font-size: 17px;
    line-height: 100%;
    letter-spacing: 0.3px;
    color: #DA5D24;
  }
  .expertise__area-index::after {
    content: '';
    display: block;
    width: 13px;
    height: 13px;
    margin-left: 21px;
    background: url('@/assets/expertise/svg/area-index-icon.svg') center / contain no-repeat;
  }
  .expertise__area-text {
    display: inline-block;
    margin-top: 180px;
    font-family: Mulish;
    font-weight: 800;
    font-size: 17px;
    line-height: 100%;
    letter-spacing: 0.3px;
    color: #2F3034;
  }
  .expertise__area:hover {
    background: url('@/assets/expertise/png/area-background_hover.png');
    background-repeat: no-repeat;
    background-size: auto 100%;
    background-position: 55% center;
    
  }
  .expertise__area:hover .expertise__area-index{
    color: white;
  }
  .expertise__area:hover .expertise__area-index::after {
    background: url('@/assets/expertise/svg/area_index_icon-hover.svg') center / contain no-repeat;
  }
  .expertise__area:hover .expertise__area-text {
    color: white;
  }


</style>
