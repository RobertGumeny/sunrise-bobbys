<template>
  <div class="desktopNav">
    <ul>
      <li><nuxt-link to="/">Home</nuxt-link></li>
      <span>|</span>
      <li><nuxt-link to="/">Locations</nuxt-link></li>
      <span>|</span>
      <li><nuxt-link to="/">About</nuxt-link></li>
      <span>|</span>
      <li><nuxt-link to="/">Catering</nuxt-link></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "desktopNav",
  data() {
    return {};
  },
  computed: {},
  methods: {},
  components: {}
};
</script>

<style lang="scss" scoped>
.desktopNav {
  color: $text-secondary;
  text-align: center;
  margin: 0.75em 0;
}
ul {
  display: flex;
  flex-direction: row;
  justify-content: center;
  padding: 0;
  list-style: none;
}
ul a {
  margin: 0.6em;
  text-decoration: none;
  color: $text-secondary;
}
@media screen and (min-width: 768px) {
  ul a {
    margin: 0.4em;
  }
}
@media screen and (min-width: 992px) {
  ul a {
    margin: 1em;
  }
}
@media screen and (min-width: 1200px) {
  ul a {
    margin: 1.4em;
  }
}
</style>
