<script setup>
  const props = defineProps({
    groups: {
      type: Array,
      required: true,
    },
  })
</script>

<template>
  <section class="about" id="our-company">
    <div class="about__values">
      <div class="about__values-container">
        <header class="about__values-intro">
          <div class="about__values-heading">
            <span class="about__values-eyebrow">
              Holistic. Agile. Reliable
            </span>

            <h2 class="about__values-title">
              With this triad we line up to support you to realize your projects successfully. 
            </h2>
          </div>
          
          <div class="about__values-description">
            <p class="about__values-paragraph about__values-paragraph--p1a">
              Today’s construction projects are notable for the diversity of their requirements. While you want your 
              buildings to be safe, economical, and durable, they primarily serve your operations. Our deep industry 
              knowledge helps to optimally incorporate the variety of usage requirements of the cement
            </p>
            <div class="container">
              <p class="about__values-paragraph about__values-paragraph--p1b">
                production processes into civil design.
              </p>

              <p class="about__values-paragraph about__values-paragraph--p2">
                We constantly achieve client success by following these three core values for all projects our clients 
                trust us with.
              </p>
            </div>
            
          </div>
        </header>

        <ul class="about__values-list">
          <li class="about__value about__value--holistic">
            <h3 class="about__value-title">
              <span>Holistic</span>
              <span>planning</span>
            </h3>
            <p class="about__value-description">
              Through continuous consideration of all circumstances, we create futureproof buildings and frictionless 
              construction workflows. Systematic implementation of this holistic approach helps us to keep the 
              bird’s-eye view over all interfaces. We are proactively making sure that all included parties can focus 
              on working towards the optimal project result.
            </p>
          </li>
          
          <li class="about__value about__value--agile">
            <h3 class="about__value-title">
              <span>Agile</span>
              <span>acting</span>
            </h3>
            <p class="about__value-description">
              Our team can put results down on paper rapidly. In a world that is increasingly characterized by changing 
              and adapting to uncertain circumstances, we can flexibly execute on multiple iterations of the project in 
              close consultation with the client. This allows us to cater to your construction needs until the last 
              phases of planning.
            </p>
          </li>

          <li class="about__value about__value--reliable">
            <h3 class="about__value-title">
              <span>Reliable</span>
              <span>realisation.</span>
            </h3>
            <p class="about__value-description">
              We prioritize project success over everything. Based on our decades of experience we have developed the 
              highest quality standards and demonstrate with every new project our commitment to meeting and exceeding 
              client expectations. 
            </p>
          </li>
        </ul>
      </div>
      
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

      <section class="about__team-group">
        <h3 class="about__team-group-title">
          Leadership Team
        </h3>
        <ul class="about__team-list team team--leadership">
          <li class="team__member team__member--leadership">
            <div class="team__member-avatar team__member-avatar--leadership team__member-avatar--ceo">
              <img
                src="@/assets/about/png/leonardo dicaprio.png"
                alt=""
              />
            </div>
            
            <div class="team__member-info team__member-info--leadership">
              <h4 class="team__member-name team__member-name--leadership">
                Tim-Nicolas Mollenhauer
              </h4>
              <span class="team__member-position">
                CEO
              </span>
              <p class="team__member-bio team__member-bio--ceo">
                Viverra in turpis vitae tincidunt. Odio nunc netus consectetur libero duis. Est quis vitae, sed egestas 
                vehicula.
              </p>
              <a href="#" class="team__member-linked-in">
                <img
                  class="team__member-icon team__member-icon--hover"
                  src="@/assets/about/svg/linked in hover.svg"
                  alt=""
                  aria-hidden="true"
                >
                <img
                  class="team__member-icon team__member-icon--default"
                  src="@/assets/about/svg/linked in.svg"
                  alt=""
                  aria-hidden="true"
                >
              </a>
            </div>
          </li>

          <li class="team__member team__member--leadership">
            <div class="team__member-avatar team__member-avatar--leadership team__member-avatar--creative">
              <img
                src="@/assets/about/png/Ben Stiller.png"
                alt=""
              />
            </div>
            <div class="team__member-info team__member-info--leadership">
              <h4 class="team__member-name team__member-name--leadership">
                Klaus-Dieter Mollenhauer
              </h4>
              <span class="team__member-position">
                Creative Director
              </span>
              <p class="team__member-bio team__member-bio--creative-director">
                Duis aenean ultricies ullamcorper neque cras vel. Quam sem turpis est morbi nunc odio feugiat 
                pellentesque. Eget risus lectus donec tempus cras. Amet amet, auctor habitasse tristique pellentesque 
                id velit.
              </p>
              <a href="#" class="team__member-linked-in">
                <img
                  class="team__member-icon team__member-icon--hover"
                  src="@/assets/about/svg/linked in hover.svg"
                  alt=""
                  aria-hidden="true"
                >
                <img
                  class="team__member-icon team__member-icon--default"
                  src="@/assets/about/svg/linked in.svg"
                  alt=""
                  aria-hidden="true"
                >
              </a>
            </div>
            
          </li>
        </ul>
      </section>

      <div class="about__team-groups">
        <section 
          v-for="(group, groupIndex) in groups"
          :key="group.id"
          class="about__team-group"
          :class="'about__team-' + group.class"
        >
          <h3 class="about__team-group-title">
            {{ group.title }}
          </h3>

          <ul class="about__team-list team">
            <li
              v-for="(member, memberIndex) in group.members"
              :key="member.id"
              class="team__member"
              :class="{
                'team__member-decorated' : groupIndex === groups.length - 1 && memberIndex === 0
              }"
            >
              <img
                :src="member.avatar"
                alt=""
                aria-hidden="true"
                class="team__member-avatar"
              />
              <div class="team__member-info">
                <div class="team__member-heading">
                  <h4 class="team__member-name">
                    <span
                      v-for="(word, i) in member.name.split(' ')"
                      :key="i"
                    >
                      {{ word }}
                    </span>
                  </h4>
                  <a
                    v-if="member.cta"
                    class="team__member-apply-button"
                    :href="member.cta.link"
                  >
                    <span>
                      {{ member.cta.label }}
                    </span>
                  </a>
                </div>
                
                <span class="team__member-position">
                  {{ member.position }}
                </span>
              </div>
            </li>
          </ul>
        </section>
      </div>  
    </div>
  </section>
</template>

<style scoped>
  .about {
    margin-top: 184px;
  }
  .about__values {
    display: flex;
    justify-content: center;
  }
  .about__values-intro {
    display: flex;
    gap: 90px;
  }
  .about__values-heading {
    width: 344px;
    flex-shrink: 0
  }
  .about__values-heading::after {
    content: '';
    margin-top: 40px;
    width: 100%;
    height: 100%;
    display: block;
    background: url('@/assets/about/svg/Arrow 3.svg') no-repeat;
  }
  .about__values-eyebrow {
    font-weight: 400;
    font-style: Regular;
    font-size: 18px;
    line-height: 130%;
    letter-spacing: 0.3px;
  }
  .about__values-title {
    margin-top: 24px;
    max-width: 298px;
    font-weight: 400;
    font-style: Regular;
    font-size: 32px;
    line-height: 100%;
    letter-spacing: -1px;
    color: #DA5D24;
  }
  .about__values-description {
    margin-top: 47px;
    display: flex;
    gap: 39px;
    font-weight: 600;
    font-style: SemiBold;
    font-size: 16px;
    line-height: 140%;
    letter-spacing: 0.3px;
  }
  .about__values-paragraph--p1a {
    max-width: 322px;
  }
  .about__values-paragraph--p1b {
    max-width: 285px;
  }
  .about__values-paragraph--p2 {
    margin-top: 22px;
    max-width: 285px;
  }
  .about__values-list {
    margin-left: 434px;
    margin-top: 55px;
    display: flex;
    flex-wrap: wrap;
    gap: 82px;
  }
  .about__value--holistic {
    max-width: 285px;
  }
  .about__value--agile {
    max-width: 275px;
  }
  .about__value--reliable {
    max-width: 267px;
  }
  .about__value-title {
    display: flex;
    flex-direction: column;
    font-weight: 900;
    font-size: 28px;
    line-height: 120%;
    letter-spacing: -1px;
    color: #313131;
  }
  .about__value-description {
    margin-top: 24px;
    font-weight: 400;
    font-size: 16px;
    line-height: 140%;
    letter-spacing: 0.3px;
    color: #737B7D;
  }

  .about__team {
    margin-top: 184px;
    padding: 0 70px 0 147px;
  }
  .about__team-intro {
    margin-left: 81px;
  }
  .about__team-title {
    font-weight: 700;
    font-style: Bold;
    font-size: 40px;
    line-height: 100%;
    letter-spacing: -1px;
  }
  .about__team-subtitle {
    margin-top: 40px;
    max-width: 445px;
    font-weight: 400;
    font-style: Regular;
    font-size: 32px;
    line-height: 100%;
    letter-spacing: -1px;
    color: #DA5D24;
  }
  .about__team-group {
    display: flex;
  }
  .about__team-groups {
    display: flex;
    justify-content: flex-start;
    flex-wrap: wrap;
    column-gap: 144px;
  }
  .about__team-group-title {
    width: 40px;
    height: 345px;
    position: relative;
    
    font-weight: 300;
    font-size: 32px;
    line-height: 100%;
    letter-spacing: 0px;
    color: #0E0E0C;
    writing-mode: vertical-rl;
    transform: rotate(180deg);
    align-self: end;
  }
  .about__team-group-title::before {
    content: "";
    position: absolute;
    z-index: -1;
    top: -5px;
    bottom: 75.4%;
    left: 6px;
    right: 9px;
    background: #FF7C40;
  }
  .team {
    margin-left: 44px;
    margin-top: 78px;

    display: flex;
    flex-wrap: wrap;
    column-gap: 1px;
    row-gap: 45px;
  }
  .team::after {
    content: '';
    width: 100%;
    height: 1px;
    background: repeating-linear-gradient(
      to right,
      #2F3034 0 8px,
      transparent 1px 16px
  );
  }
  .team--leadership {
    display: flex;
    justify-content: space-evenly;
    row-gap: 41px;
  }
  .team--leadership::after {
    content: '';
    width: 100%;
    height: 1px;
    margin-top: 52px;
    background: repeating-linear-gradient(
      to right,
      #2F3034 0 8px,
      transparent 1px 16px
    );
  }
  .team__member {
    display: flex;
    flex-direction: column;
  }
  .team__member-decorated{
    position: relative;
  }
  .team__member-decorated::after {
    content: "";
    position: absolute;
    left: 163px;
    top: 42px;
    width: 64px;
    height: 174px;
    background: #FF7C40;
    transform: skewX(-10deg);
    z-index: 0;
  }
  .team__member-decorated .team__member-avatar,
  .team__member-decorated .team__member-info {
    position: relative;
    z-index: 1;
  }
  .team__member--leadership {
    flex-direction: row;
  }
  .team__member-avatar {
    width: 215px;
    height: 216px;
  }
 
  .team__member-avatar--ceo::after {
    content: "";
    position: absolute;
    z-index: -1;
    right: -30px;
    top: 155px;
    width: 64px;
    height: 190px;
    background: #DA5D24;
    clip-path: polygon(
      0% 5%,
      100% 0%,
      53% 100%,
      0% 92%
    );
  }
  .team__member-avatar--creative::after {
    content: "";
    position: absolute;
    z-index: -1;
    left: 30px;
    bottom: -30px;
    width: 200px;
    height: 48px;
    background: #0D2B7A;
    clip-path: polygon(
      3% 20%,
      100% 0%,
      100% 30%,
      0% 100%
    );
  }
  .team__member-avatar--leadership {
    position: relative;
    width: 287px;
    height: 345px;
    z-index: 0;
  }
  .team__member-avatar--leadership img {
    position: relative;
    width: 100%;
    height: 100%;
    object-fit: cover;
    z-index: 1;
  }
  .team__member-info {
    max-width: 216px;
  }
  .team__member-heading {
    margin-top: 16px;
    display: flex;
    position: relative;
  }
  .team__member-apply-button {
    position: absolute;
    width: 84px;
    height: 24px;
    margin-left: 61px;
    border-radius: 13px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #FF7C40;
    font-weight: 600;
    font-style: SemiBold;
    font-size: 13px;
    line-height: 120%;
    letter-spacing: 0px;
    color: white;
    transition: 0.3s ease;
  }
  .team__member-apply-button:hover {
    background-color: #DA5D24;
  }
  .team__member-info--leadership {
    margin-left: 46px;
    width: 346px;
    max-width: 346px;
  }
  .team__member-name {
    font-weight: 700;
    font-style: Bold;
    font-size: 20px;
    line-height: 120%;
    letter-spacing: 0px;
  }
  .team__member-name span {
    display: block;
  }
  .team__member-name--leadership {
    font-weight: 700;
    font-style: Bold;
    font-size: 36px;
    line-height: 100%;
    letter-spacing: 0px;
  }
  .team__member-position {
    margin-top: 16px;
    display: inline-flex;
    align-items: center;
    gap: 16px;
    max-width: 210px;
    font-weight: 400;
    font-style: Regular;
    font-size: 16px;
    line-height: 100%;
    letter-spacing: 0px;
  }
  .team__member-position::before {
    content: '';
    min-width: 21px;
    height: 16px;
    background: url('@/assets/about/svg/Arrow 4.svg') no-repeat;
  }
  .team__member-bio {
    margin-top: 16px;
    font-weight: 400;
    font-size: 16px;
    line-height: 22px;
    letter-spacing: 0.3px;
    color: #737B7D;
  }
  .team__member-bio--ceo {
    max-width: 224px;
  }
  .team__member-bio--creative-director {
    max-width: 259px;
  }
  .team__member-linked-in {
    margin-top: 34px;
    display: inline-block;
    position: relative;
  }
  .team__member-icon {
    position: absolute;
    transition: 0.2s ease;
  }
  .team__member-linked-in:hover .team__member-icon--default {
    opacity: 0;
  }
</style>