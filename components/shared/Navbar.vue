<template>
  <nav class="navbar" role="navigation" aria-label="main navigation">
    <NavbarBrand v-on:burgerClicked="toggleMenu"/>
    <NavbarMenu :class="{'is-active': isMenuActive}"/>
  </nav>
</template>

<script>
import NavbarBrand from "~/components/shared/Navbar/NavbarBrand";
import NavbarMenu from "~/components/shared/Navbar/NavbarMenu";
export default {
  name: "Navbar",
  components: {NavbarMenu, NavbarBrand},
  data() {
    return {
      isMenuActive: false
    }
  },
  methods: {
    toggleMenu(isActive) {
      this.isMenuActive = isActive
    }
  }
}
</script>
