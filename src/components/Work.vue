<template>
  <section class="section is-medium">
    <div class="container">
      <div class="columns content is-large">
        <div class="column is-offset-2">
          <p class="highlight">Latest work</p>
        </div>
      </div>
      <div class="columns content is-large">
        <div class="column is-6 is-offset-2">
          <p class="title">eDreams ODIGEO Help Centre Revamp</p>
        </div>
      </div>
      <div class="columns content">
        <div class="column is-8 is-offset-2">
          <p>
            <strong>Complete redesign</strong>. Not only in terms of visual, but also
            <strong>rebuild the frontend</strong>. We
            also built a new CMS tool that allowed us to connect it through a RESTful API.
          </p>
          <p>
            I worked on the whole redesign, following a typical design process:
            <ul>
              <li>I did some <strong>research</strong> in order to collect data and understand the problems of the old version</li>
              <li>To complement that, some <strong>benchmark</strong> was also necessary</li>
              <li>When I had all the information and data, I started <strong>designing a few possible solutions</strong></li>
              <li>I did a few <strong>prototypes</strong> and tested them into the UX Lab with some users. After the sessions I discussed the learnings with the members of the Customer Service Team who were working in the project with me</li>
              <li>Finally, we decided to build the <strong>proper solution</strong>. Last step was to run an A/B test in production</li>
            </ul>
          </p>
          <p>The Revamp was made for the 4 different brands of the company.</p>
        </div>
      </div>
    </div>
    <div class="container is-fluid hero-image">
      <img src="../assets/hc.png" alt="eDO Help Centre" />
    </div>
    <div class="container">
      <div class="columns content is-large">
        <div class="column is-6 is-offset-2">
          <p class="title">eDreams ODIGEO CSS Framework</p>
        </div>
      </div>
      <div class="columns content">
        <div class="column is-8 is-offset-2">
          <p>Development, maintenance and evolution of featured <strong>eDreams ODIGEO CSS framework</strong>.</p>
          <p>The project was <strong>an initiative of the UX Design Team</strong>. The goal was to provide Frontend Devs with a set of rules and patterns to facilitate the integration of our designs, specially for the mobile web.</p>
          <p>My role here was <strong>to define and design the main elements of the framework</strong> in collaboration with other UX Designers. After that, I built the framework together with another dev workmate.</p>
        </div>
      </div>
    </div>
    <Carousel class="carousel hero-image" />
    <div class="container">
      <div class="columns content is-small">
        <div class="column is-6 is-offset-2">
          <div class="soon"><span>Current project</span></div>
        </div>
      </div>
      <div class="columns content is-large">
        <div class="column is-6 is-offset-2">
          <p class="title">eDreams ODIGEO Design System</p>
        </div>
      </div>
      <div class="columns content">
        <div class="column is-8 is-offset-2">
          <p>The build and implementation of this framework was the starting point of what would later evolve in <strong>eDreams ODIGEO Design System</strong>, what I am currently working on.</p>
        </div>
      </div>
    </div>
    <div class="container is-fluid hero-image">
      <img src="../assets/prisma.png" alt="eDO Design System" />
    </div>

    <div class="container">
      <div class="columns content is-large">
        <div class="column is-offset-2">
          <p class="highlight">Past projects</p>
        </div>
      </div>
      <div class="columns content is-large">
        <div class="column is-6 is-offset-2">
          <p class="title">Localler, Socialstats, BlackWood 7...</p>
        </div>
      </div>
      <div class="columns content">
        <div class="column is-8 is-offset-2">
          <p>This is showcase of some of my past work. If you need more information about these projects, please, <span @click="sendAnEmail">drop me a line</span>.</p>
          <button class="btn"><span>Know more</span></button>
        </div>
      </div>
    </div>
    <div class="container is-fluid hero-image">
      <img src="../assets/socialstats.png" />
      <img src="../assets/chaffoteaux.png" />
      <img src="../assets/bw7.png" />
      <img src="../assets/ilumax.png" />
    </div>
  </section>
</template>

<script>
// @ is an alias to /src
import Carousel from '@/components/Carousel.vue';

export default {
  name: 'Work',
  components: {
    Carousel,
  },
  methods: {
    sendAnEmail() {
      window.location = 'mailto:hello.alex.cerezo@gmail.com';
    },
  },
};
</script>
