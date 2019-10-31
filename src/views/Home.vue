<template>
  <article>
    <nav class="nav">
      <h1 @click="goToHome" class="my-name">Alex Cerezo</h1>
      <Menu class="is-home" />
    </nav>
    <Hero />
    <About />
    <Work />
    <Contact />
  </article>
</template>

<script>
// @ is an alias to /src
import Menu from '@/components/Menu.vue';
import Hero from '@/components/Hero.vue';
import About from '@/components/About.vue';
import Work from '@/components/Work.vue';
import Contact from '@/components/Contact.vue';

export default {
  name: 'home',
  components: {
    Menu,
    Hero,
    About,
    Work,
    Contact,
  },
  methods: {
    goToHome() {
      this.$router.push('/');
    },
  },
};
</script>
