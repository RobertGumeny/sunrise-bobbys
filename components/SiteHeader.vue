<template>
  <div class="main">
    <header>
      <img src="../assets/images/logo.png" alt="Sunrise Bobby's Logo" />
      <a href="javascript:void(0);" class="toggle" @click="toggleNav"
        ><fa :icon="['fas', 'bars']"
      /></a>
      <DesktopNav id="desktopNav"></DesktopNav>
    </header>
    <MobileNav id="mobileNav"></MobileNav>
  </div>
</template>

<script>
import MobileNav from "./MobileNav";
import DesktopNav from "./DesktopNav";
export default {
  name: "site-header",
  data() {
    return {};
  },
  computed: {},
  methods: {
    toggleNav() {
      const mobile = document.getElementById("mobileNav").classList;
      mobile.contains("show") ? mobile.remove("show") : mobile.add("show");
    }
  },
  components: {
    MobileNav,
    DesktopNav
  }
};
</script>

<style lang="scss" scoped>
.main {
  padding: 1rem;
  background-color: $bg-primary;
  color: $text-secondary;
  letter-spacing: 1.25px;
  font-family: "Lilita One", cursive;
  position: relative;
}

header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

img {
  width: 35%;
  padding: 0.2em;
}

// Mobile nav toggle displays in top right by default
a.toggle {
  color: $text-secondary;
  font-size: 2em;
  margin-right: 1em;
}

// Display mobile nav when toggle is clicked
#mobileNav {
  display: none;
}
#mobileNav.show {
  display: block;
}

// Hide desktop nav by default
#desktopNav {
  display: none;
}

@media screen and (min-width: 576px) {
  img {
    width: 30%;
    padding: 0.5em;
  }
}

@media screen and (min-width: 768px) {
  // Show desktop nav
  #desktopNav {
    display: block;
  }
  // Hide mobile nav
  #mobileNav.show {
    display: none;
  }
  // Hide toggle icon for mobile navigation
  a.toggle {
    display: none;
  }
  img {
    width: 25%;
    padding: 0.5em;
  }
}

@media only screen and (min-width: 1200px) {
  img {
    width: 22.5%;
    padding: 1em;
  }
}
</style>
