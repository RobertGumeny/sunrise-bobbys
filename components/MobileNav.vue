<template>
  <div class="mobileNav">
    <ul>
      <li><nuxt-link to="/">Home</nuxt-link></li>
      <li><nuxt-link to="/">Locations</nuxt-link></li>
      <li><nuxt-link to="/">About</nuxt-link></li>
      <li><nuxt-link to="/">Catering</nuxt-link></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "mobileNav",
  data() {
    return {};
  },
  computed: {},
  methods: {},
  components: {}
};
</script>

<style lang="scss" scoped>
.mobileNav {
  text-align: center;
  font-size: 1.2em;
}
ul {
  padding: 0;
  list-style: none;
}
ul a {
  display: block;
  color: $text-secondary;
  text-decoration: none;
  margin: 0.5em 0em;
}
</style>
