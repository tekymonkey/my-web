<template>
  <article>
    <nav class="nav">
      <h1 @click="goToHome" class="my-name">Alex Cerezo</h1>
      <Menu class="is-home" />
    </nav>
    <Hero />
    <About />
    <Work />
    <Carousel />
    <Contact />
  </article>
</template>

<script>
// @ is an alias to /src
import Menu from '@/components/Menu.vue';
import Hero from '@/components/Hero.vue';
import About from '@/components/About.vue';
import Work from '@/components/Work.vue';
import Carousel from '@/components/Carousel.vue';
import Contact from '@/components/Contact.vue';

export default {
  name: 'home',
  components: {
    Menu,
    Hero,
    About,
    Work,
    Carousel,
    Contact,
  },
  methods: {
    goToHome() {
      this.$router.push('/');
    },
  },
};
</script>
