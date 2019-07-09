<template>
  <section class="section is-medium">
    <div class="container">
      <div class="columns content is-large">
        <div class="column is-offset-2">
          <p class="highlight">Latest work</p>
        </div>
      </div>
      <div class="columns content is-large">
        <div class="column is-5 is-offset-2">
          <p class="title">eDO Help Centre Revamp</p>
        </div>
      </div>
      <div class="columns content is-large">
        <div class="column is-5 is-offset-2">
          <p>
            <strong>Complete redesign</strong>. Not only in terms of visual, but also
            <strong>rebuild the frontend</strong>. We
            also looked for a new CMS that allowed us to connect it through a RESTful API.
          </p>
          <p>The Revamp was made for the 4 different brands of the company.</p>
          <div class="more disabled">
            <p>
              Read more
              <IconArrow />
            </p>
          </div>
          <div class="warn content is-small">Coming soon</div>
        </div>
      </div>
    </div>
    <div class="container is-fluid hero-image">
      <img src="../assets/hc.png" alt="eDO Help Centre" />
    </div>
    <div class="container">
      <div class="columns content is-large">
        <div class="column is-5 is-offset-2">
          <p class="title">eDO CSS Framework / Design System</p>
          <p>Development, maintenance and evolution of featured eDreams ODIGEO CSS framework.</p>
          <p>
            The build and implementation of this framework was
            the starting point of what would later evolve in
            <strong>
              eDO
              Design System
            </strong>, which I am currently working on.
          </p>
          <p>Interested into talk about this project?</p>
          <button class="btn">
            <span @click="SendAnEmail">Drop me a line</span>
          </button>
        </div>
        <div class="column is-offset-1 is-iconcss">
          <IconCSS />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
// @ is an alias to /src
import IconArrow from '@/components/IconArrow.vue';
import IconCSS from '@/components/IconCSS.vue';

export default {
  name: 'Work',
  components: {
    IconArrow,
    IconCSS,
  },
  methods: {
    SendAnEmail() {
      window.location = 'mailto:hello.alex.cerezo@gmail.com';
    },
  },
};
</script>
