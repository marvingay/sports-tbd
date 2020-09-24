<template>
  <header class="header">
    <h1 class="logo">XYMXN</h1>
    <div id="nav">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
    </div>
  </header>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Header',
});
</script>

<style lang="scss" scoped>
.header {
  background: #fff;
  box-shadow: 0 0 16px 0 rgba(0, 0, 0, 0.3);
  display: flex;
  z-index: 10;

  .logo {
    color: #c70000;
  }

  #nav {
    padding: 30px;

    a {
      font-weight: bold;
      color: black;
      text-decoration: none;

      &:hover {
        color: #c70000;
      }

      &.router-link-exact-active {
        color: #c70000;
      }
    }
  }
}
</style>
