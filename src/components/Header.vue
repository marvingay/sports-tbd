<template>
  <header class="header">
    <div id="logo">
      <h1 class="logo">XYMXN</h1>
    </div>
    <div id="nav">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/games">Games</router-link>
      <router-link to="/picks">Picks</router-link>
    </div>
    <div id="userOptions">
      <button><router-link to="/signup">Join</router-link></button>
      <router-link to="/login">Login</router-link>
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
  align-items: center;
  background: #fff;
  box-shadow: 0 0 16px 0 rgba(0, 0, 0, 0.3);
  display: flex;
  justify-content: space-around;
  position: sticky;
  text-transform: uppercase;
  top: 0;
  z-index: 10;

  #logo {
    display: flex;
    flex: 1;
    .logo {
      color: #c70000;
      font-size: 2em;
      letter-spacing: 0.2em;
      margin: 0 auto;
    }
  }

  #nav {
    justify-content: center;
    display: flex;
    flex: 3;
    padding: 30px;

    a {
      color: black;
      font-size: 1.25rem;
      font-weight: bold;
      margin: 0 15px;
      padding: 10px 0;
      text-decoration: none;

      &:hover {
        color: #c70000;
      }

      &.router-link-exact-active {
        border-bottom: 2px solid #c70000;
        color: #c70000;
      }
    }
  }

  #userOptions {
    flex: 1;

    a {
      color: black;
      font-size: 1.25rem;
      margin: 0 15px;
      padding: 10px 0;
      text-decoration: none;

      &:hover {
        color: #c70000;
      }
    }
  }
}
</style>
