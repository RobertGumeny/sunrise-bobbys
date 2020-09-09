<template>
  <div>
    <SiteHeader />
    <Nuxt />
  </div>
</template>

<script>
import SiteHeader from "../components/SiteHeader";
export default {
  components: {
    SiteHeader
  }
};
</script>

<style lang="scss">
// Primary Font
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;700&display=swap");

// Header/Navbar Font
@import url("https://fonts.googleapis.com/css2?family=Lilita+One&display=swap");

html {
  font-family: "Open Sans", sans-serif;
  font-size: 14px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  scroll-behavior: smooth;
}
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

@media only screen and (min-width: 360px) {
  body {
    font-size: 18px;
  }
}
@media only screen and (min-width: 576px) {
  body {
    font-size: 20px;
  }
}
@media only screen and (min-width: 850px) {
  body {
    font-size: 24px;
  }
}
@media only screen and (min-width: 1199px) {
  body {
    font-size: 26px;
  }
}
</style>
