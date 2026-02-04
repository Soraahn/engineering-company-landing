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
</template>

<style scoped>
  
</style>