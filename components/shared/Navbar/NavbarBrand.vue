<template>
  <div class="navbar-brand">
    <NuxtLink to="/" class="navbar-item">
      <NavbarLogo/>
    </NuxtLink>

    <NavbarBurger :showNav="false"/>
  </div>
</template>

<script>
import NavbarBurger from "~/components/shared/Navbar/NavbarBurger";
import NavbarLogo from "~/components/shared/Navbar/NavbarLogo";
export default {
  name: "NavbarBrand",
  components: {NavbarLogo, NavbarBurger},
}
</script>
