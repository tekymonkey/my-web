<template>
  <section class="section is-medium">
    <div class="container">
      <div class="columns content is-large">
        <div class="column is-offset-2">
          <p class="highlight">
            Product Design / UX Research /
            Prototyping / Frontend Development
          </p>
        </div>
      </div>
      <div class="columns content is-large">
        <div class="column is-4 is-offset-2">
          <p class="subtitle is-3">
            User focus. Problem-solver. Advocate of exceptional design.
            More than 10 years designing, developing
            and scaling projects for several product companies.
          </p>
        </div>
        <div class="column is-4">
          <p>
            I weave together <strong>strong design aesthetics with technical know-how</strong>.
            I partner with UX Researchers and UX Designers to <strong>define and deliver new features</strong>,
            translate concepts into living <strong>prototypes</strong>, and iterate on interactions,
            animations, and details to deliver the <strong>perfect experience</strong>.
          </p>
          <p>
            Currently interested and working with
            <strong>Design Systems</strong> and LEAN methodologies.
          </p>
          <button @click="goToLinkedin" class="btn">
            <span>Linkedin Profile</span>
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'About',
  methods: {
    goToLinkedin() {
      window.open('https://www.linkedin.com/in/alexcerezo/', '_blank');
    },
  },
};
</script>
