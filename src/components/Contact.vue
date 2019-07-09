<template>
  <div>
    <footer class="footer">
      <div class="content has-text-centered">
        <div class="soon">
          <span>More examples, projects and cases studies to be added soon.</span>
        </div>
        <div class="columns content is-large">
          <div class="column is-6 is-offset-3">
            <span class="display">Get in touch</span>
            <p>
              Did you like it?
              If you are interested into my work or
              just want to get your ass kicked in FIFA for PS4,
              please feel free to contact me at
              <span
                @click="sendAnEmail"
                class="is-underline"
              >hello.alexcerezo@gmail.com</span> or
              <span @click="goToTwitter" class="is-underline">Twitter</span>.
            </p>
          </div>
        </div>
        <div class="links">
          <button @click="goToLinkedin" class="btn link-item">
            <span>Linkedin Profile</span>
          </button>
          <button @click="sendAnEmail" class="btn link-item">
            <span>Send me an Email</span>
          </button>
        </div>
      </div>
    </footer>
    <Menu class="is-last" />
  </div>
</template>

<script>
// @ is an alias to /src
import Menu from '@/components/Menu.vue';

export default {
  name: 'Contact',
  components: {
    Menu,
  },
  methods: {
    sendAnEmail() {
      window.location = 'mailto:hello.alex.cerezo@gmail.com';
    },
    goToLinkedin() {
      window.open('https://www.linkedin.com/in/alexcerezo/', '_blank');
    },
    goToTwitter() {
      window.open('https://twitter.com/tekymonkey', '_blank');
    },
  },
};
</script>

<style lang="scss" scoped>
.contact {
  text-align: center;
}
</style>
