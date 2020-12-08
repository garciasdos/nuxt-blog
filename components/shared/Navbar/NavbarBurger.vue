<template>
  <div class="navbar-burger" @click="toggleBurger" :class="{ 'is-active': isActive }">
    <span aria-hidden="true"></span>
    <span aria-hidden="true"></span>
    <span aria-hidden="true"></span>
  </div>
</template>

<script>
export default {
  props: {
    showNav: Boolean
  },
  name: "NavbarBurger",
  data: function () {
    return {
      isActive: this.showNav
    }
  },
  methods: {
    toggleBurger() {
      this.isActive = !this.isActive;
      this.$parent.$emit('burgerClicked', this.isActive)
    }
  }
}
</script>
