<template>
  <div class="main">
    <header>
      <img src="../assets/images/logo.png" alt="Sunrise Bobby's Logo" />
      <nav class="collapsed">
        <a
          href="javascript:void(0);"
          @click="$event.target.classList.toggle('responsive')"
          ><fa :icon="['fas', 'bars']"
        /></a>
      </nav>
      <nav class="navMain" id="navMain">
        <a href="#">Home</a>
        <span>|</span>
        <a href="#">Locations</a>
        <span>|</span>
        <a href="#">About</a>
        <span>|</span>
        <a href="#">Catering</a>
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
  font-family: "Lilita One", cursive;
}
header {
  display: flex;
  flex-direction: row;
  margin-bottom: 1em;
  position: relative;
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

nav.navMain {
  display: none;
}

nav.navMain.responsive {
  position: relative;
}
nav.navMain a {
  float: none;
  display: block;
  text-align: left;
}

nav.collapsed {
  font-size: 2.25em;
  position: absolute;
  top: 50%;
  left: 85%;
  transform: translate(0%, -50%);
}

a.orderOnline {
  color: $text-secondary;
  background-color: $text-primary;
  border: 1px solid $text-primary;
  border-radius: 5px;
  padding: 5px 10px;
  text-align: center;
  display: block;
}

@media only screen and (min-width: 576px) {
  header {
    display: block;
    text-align: center;
  }
  nav.collapsed {
    display: none;
  }
  nav.navMain {
    display: block;
  }
  .main {
    text-align: center;
  }
  a.orderOnline {
    display: inline-block;
    margin-bottom: 0.5em;
  }
}
@media only screen and (min-width: 690px) {
  img {
    width: 45%;
  }
}
@media only screen and (min-width: 850px) {
  img {
    width: 35%;
  }
}
@media only screen and (min-width: 1040px) {
  img {
    width: 25%;
  }
}
@media only screen and (min-width: 1199px) {
  img {
    width: 20%;
  }
}
</style>
