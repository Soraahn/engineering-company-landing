<script setup>
  const navLinks = [
    {label: "Services", href: "#services", class: "navigation-bar__services", id: crypto.randomUUID()},
    {label: "Projects & References", href: "#projects-and-references", class: "navigation-bar__projects-and-references", id: crypto.randomUUID()},
    {label: "Our Company", href: "#our-company", class: "navigation-bar__our-company", id: crypto.randomUUID()},
    {label: "Careers", href: "#careers", class: "navigation-bar__careers", id: crypto.randomUUID()},
  ];

  import {ref} from 'vue';
  const currentLang = ref('en');
  
  function setLanguage(lang) {
    currentLang.value = lang;
  }
  
  import firstServicesImage from '@/assets/services/svg/image 85 (1).svg';
  import secondServicesImage from '@/assets/services/svg/image_85.svg';

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
      src: firstServicesImage,
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
      src: secondServicesImage,
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

  const groups = [
    {
      id: 1,
      class: 'engineers',
      title: 'Engineers',
      members: [
        {
          id: crypto.randomUUID(),
          avatar: 'src/assets/about/png/Natalie Portman.png',
          name: 'Bernhard Meyer',
          position: 'Senior Steel Structures Engineer'
        },
        { 
          id: crypto.randomUUID(),
          avatar: 'src/assets/about/png/Emma Stone.png',
          name: 'Alexander Jung',
          position: 'Project Engineer'
        },
        {
          id: crypto.randomUUID(),
          avatar: 'src/assets/about/png/Joaquin Phoenix.png',
          name: 'Stefan Schniedermeier',
          position: 'Project Engineer'
        },
        {
          id: crypto.randomUUID(),
          avatar: 'src/assets/about/png/Jessica Chastain.png',
          name: 'Stefan Wiek',
          position: 'Project Engineer'
        },
        {
          id: crypto.randomUUID(),
          avatar: 'src/assets/about/png/you.png',
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
          avatar: 'src/assets/about/png/Morgan Freeman.png',
          name: 'Domenik Schmidt',
          position: 'Head of Layout & Design'
        },
        {
          id: crypto.randomUUID(),
          avatar: 'src/assets/about/png/Florence Pugh.png',
          name: 'Manuela Sonntag',
          position: 'Reinforcement Technician'
        },
        {
          id: crypto.randomUUID(),
          avatar: 'src/assets/about/png/Natalie Portman.png',
          name: 'Mark Peters',
          position: 'Planning Permission Design'
        },
        {
          id: crypto.randomUUID(),
          avatar: 'src/assets/about/png/Emma Stone.png',
          name: 'Katarina Maslanova',
          position: 'Structural Drawings'
        },
        {
          id: crypto.randomUUID(),
          avatar: 'src/assets/about/png/Joaquin Phoenix.png',
          name: 'Benedikt Schröder-Schlüter',
          position: 'Structural Drawings'
        },
        {
          id: crypto.randomUUID(),
          avatar: 'src/assets/about/png/Jessica Chastain.png',
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
          avatar: 'src/assets/about/png/Joaquin Phoenix.png',
          name: 'Najwa Hasan',
          position: 'Position'
        },
        {
          id: crypto.randomUUID(),
          avatar: 'src/assets/about/png/Jessica Chastain.png',
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
          avatar: 'src/assets/about/png/Florence Pugh.png',
          name: 'Michelle Michalik',
          position: 'Assistent to the Management'
        }
      ]
    }
  ];

  import Header from '@/components/Header.vue';
  import Services from '@/components/Services.vue';
  import Expertise from '@/components/Expertise.vue';
  import About from '@/components/About.vue';
  import Footer from '@/components/Footer/Footer.vue';

</script>

<template>
  <div class="page-wrapper">
    <Header
      :nav-links="navLinks"
      :current-lang="currentLang"
      @change-lang="setLanguage"
    />

    <Services
      :first-services-image="firstServicesImage"
      :second-services-image="secondServicesImage"
      :services-items="servicesItems"
    />

    <Expertise
      :expertise-areas="expertiseAreas"
    />
    
    <About
      :groups="groups"
    />

    <Footer
    
    />
  </div>
</template>

<style scoped>
  .page-wrapper {
    max-width: 1728px;
    margin: 0 auto;
  }
</style>