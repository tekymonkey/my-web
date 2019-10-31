<template>
  <div id="app" :class="{ nikel: nikel }">
    <router-view />
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      nikel: false,
      allowedKeys: {
        78: 'n',
        73: 'i',
        75: 'k',
        69: 'e',
        76: 'l',
      },
      konamiCodePosition: 0,
      nikelCode: ['n', 'i', 'k', 'e', 'l'],
      nikelCodePosition: 0,
    };
  },
  methods: {
    nikeling() {
      console.log('This website is so Nikel!');
      // this.nikel = true;
    },
  },
  created() {
    document.addEventListener('keydown', (e) => {
      // get the value of the key code from the key map
      const key = this.allowedKeys[e.keyCode];
      // get the value of the required key from the konami code
      const requiredKey = this.nikelCode[this.nikelCodePosition];

      // compare the key with the required key
      if (key === requiredKey) {
        // move to the next key in the konami code sequence
        // eslint-disable-next-line
        this.nikelCodePosition++;

        // if the last key is reached, activate cheats
        if (this.nikelCodePosition === this.nikelCode.length) {
          this.nikeling();
          this.nikelCodePosition = 0;
        }
      } else {
        this.nikelCodePosition = 0;
      }
    });
  },
};
</script>

<style lang="scss">
// @import url("https://fonts.googleapis.com/css?family=Berkshire+Swash&display=swap");
:root {
  --main-bg-color: #0b0b0b;
  --main-text-color: #ffffff;
  --sec-text-color: #525252;
  --main-bg-warn: #331600;
  --main-text-warn: #ff6d00;
}
html {
  background: var(--main-bg-color) !important;
  color: var(--main-text-color) !important;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}
body {
  background: var(--main-bg-color) !important;
  color: var(--main-text-color) !important;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}
.nikel {
  background-color: red;
}
.pablo {
  position: absolute;
  left: 50%;
  width: 500px;
  margin-left: -250px; /* Half the width */
}
.content h1,
.content h2,
.content h3,
.content h4,
.content h5,
.content h6 {
  color: var(--main-text-color) !important;
}
strong {
  color: var(--main-text-color) !important;
}
img + img {
  margin-top: 5rem;
}
.nav {
  display: flex;
  flex-flow: row nowrap;
  align-items: center;
  justify-content: space-between;
  padding: 2rem 3rem;
  .my-name {
    font-size: 2rem;
    font-weight: 600;
    line-height: 1.4;
    &:hover {
      cursor: pointer;
    }
  }
}
.menu {
  display: flex;
  flex-flow: row nowrap;
  align-items: center;
  justify-content: center;
  .menu-item {
    display: flex;
    flex-flow: row nowrap;
    align-items: center;
    transition: color 0.2s ease-in-out;
    &:hover {
      cursor: pointer;
      color: var(--sec-text-color);
      transition: color 0.2s ease-in-out;
    }
  }
  .menu-item:not(:last-child) {
    margin-right: 1rem;
  }
}
.links {
  display: flex;
  flex-flow: row nowrap;
  align-items: center;
  justify-content: center;
  .link-item {
    display: flex;
    flex-flow: row nowrap;
    align-items: center;
    transition: color 0.2s ease-in-out;
    &:hover {
      cursor: pointer;
      color: var(--sec-text-color);
      transition: color 0.2s ease-in-out;
    }
  }
  .link-item:not(:last-child) {
    margin-right: 1rem;
  }
}
.highlight {
  color: var(--sec-text-color);
  font-weight: 600;
}
.display {
  color: var(--main-text-color);
  font-size: 6rem;
  font-weight: 600;
  line-height: 1.4;
}
.is-underline {
  text-decoration: underline;
  &:hover {
    cursor: pointer;
  }
}
.more {
  &.disabled {
    color: var(--sec-text-color);
  }
}
.is-last {
  padding-bottom: 1rem;
}
.hc {
  background-color: transparent;
  background-image: url("./assets/framework.png");
  background-position: center center;
  background-repeat: repeat-y;
  background-size: auto;
  min-height: 615px;
  width: 100%;
}
.custom-list {
  margin-top: 0;
  margin-bottom: 0;
}
.warn {
  padding: 8px;
  background: var(--main-bg-warn);
  color: var(--main-text-warn);
  border-radius: 8px;
  font-weight: 600;
  margin-top: 8px;
  float: left;
}
.hero-image {
  padding: 5rem 0;
  &.carousel {
    margin-right: -1.5rem;
    margin-left: -1.5rem;
  }
}
.soon {
  display: flex;
  flex-flow: row nowrap;
  span {
    padding: 8px;
    background: var(--main-bg-warn);
    border-radius: 8px;
    font-weight: 600;
    margin-top: 8px;
    color: var(--main-text-warn);
  }
}
.btn {
  background: var(--sec-text-color);
  border: 0;
  position: relative;
  padding: 3px;
  display: inline-block;
  span {
    display: inline-block;
    background: var(--main-bg-color);
    color: var(--sec-text-color);
    padding: 1rem;
    font-size: 24px;
    line-height: 36px;
    transition: color 0.2s ease-in-out;
  }
  &:hover {
    cursor: pointer;
    color: var(--main-text-color);
    background: transparent;
    background-image: linear-gradient(
      90deg,
      #00c7ff 0%,
      #ffcc00 49%,
      #ff6d00 100%
    );
    span {
      color: var(--main-text-color);
      transition: color 0.2s ease-in-out;
    }
  }
}
$title-color: var(--main-text-color);
$subtitle-color: var(--main-text-color);
$title-line-height: 1.4;
$footer-background-color: transparent;
$footer-padding: 3rem 1.5rem 16rem;
@import "~bulma/bulma.sass";

// RESPONSIVE

.btn {
  @include until($desktop) {
    width: 100%;
    color: var(--main-text-color);
    background: transparent;
    background-image: linear-gradient(
      90deg,
      #00c7ff 0%,
      #ffcc00 49%,
      #ff6d00 100%
    );
    span {
      width: 100%;
      color: var(--main-text-color);
    }
  }
}
.nav {
  @include until($desktop) {
    flex-flow: column nowrap;
    align-items: flex-start;
    padding: 1rem 1.5rem;
  }
}
.is-home {
  @include until($desktop) {
    margin-left: -12px;
  }
}
.display {
  @include until($desktop) {
    font-size: 3rem;
  }
}
.hc {
  @include until($desktop) {
    display: none;
  }
}
.links {
  @include until($desktop) {
    flex-flow: column nowrap;
    .link-item:not(:last-child) {
      margin-bottom: 1.5rem;
      margin-right: 0;
    }
  }
}
.is-iconcss {
  @include until($desktop) {
    display: none;
  }
}
</style>
