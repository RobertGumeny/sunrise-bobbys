<template>
  <div class="main">
    <img src="../assets/images/logo.png" alt="Sunrise Bobby's Logo" />
    <header>
      <nav>
        <a href="#">Home</a>
        <span>|</span>
        <a href="#">Locations</a>
        <span>|</span>
        <a href="#">About</a>
        <span>|</span>
        <a href="#">Catering</a>
        <a
          href="javascript:void(0);"
          class="toggle"
          @click="$event.currentTarget.classList.toggle('responsive')"
          ><fa :icon="['fas', 'bars']"
        /></a>
      </nav>
    </header>
    <a href="#" class="orderOnline">Order Online</a>
  </div>
</template>

<script>
export default {
  name: "site-header",
  data() {
    return {};
  },
  computed: {},
  methods: {},
  components: {}
};
</script>

<style lang="scss" scoped>
.main {
  padding: 1rem;
  background-color: $bg-primary;
  color: $text-secondary;
  letter-spacing: 1.25px;
  text-align: center;
  font-family: "Lilita One", cursive;
  position: relative;
}
header {
  display: flex;
  flex-direction: row;
  justify-content: center;
  margin-bottom: 1em;
}

img {
  width: 55%;
}

nav {
  padding: 1em 0;
}

a {
  text-decoration: none;
}

nav a {
  color: $text-secondary;
}

a.toggle {
  display: none;
}

a.orderOnline {
  color: $text-secondary;
  background-color: $text-primary;
  border: 1px solid $text-primary;
  border-radius: 5px;
  padding: 5px 10px;
  text-align: center;
  display: inline-block;
}

@media only screen and (max-width: 576px) {
  nav a:not(:last-child),
  span {
    display: none;
  }
  a.toggle {
    font-size: 1.5em;
    display: block;
    position: absolute;
    top: 10%;
    left: 87.5%;
  }
  .main {
    text-align: center;
  }
  a.orderOnline {
    display: block;
    margin: -1.5em 10% 1em 10%;
  }
  nav.responsive {
    position: relative;
  }
  nav.responsive a {
    float: none;
    display: block;
    text-align: center;
  }
  @media only screen and (min-width: 690px) {
    img {
      width: 45%;
    }
  }
  @media only screen and (min-width: 850px) {
    img {
      width: 40%;
    }
    a,
    span {
      margin: 0.2em;
    }
  }
  @media only screen and (min-width: 1040px) {
    img {
      width: 32.5%;
    }
    a,
    span {
      margin: 0 0.4em;
    }
  }
  @media only screen and (min-width: 1199px) {
    img {
      width: 30%;
    }
  }
}
</style>
