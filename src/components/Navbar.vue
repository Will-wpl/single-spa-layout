<template>
  <div id="navbar">
    <b-nav class="bg-light">
      <b-nav-item href="/" v-on:click.prevent="navigateTo('/')"
        ><font-awesome-icon :icon="['fas', 'home']"/></b-nav-item
      >
      <b-nav-item href="/angular" v-on:click.prevent="navigateTo('/angular')"
        >Angular</b-nav-item
      >
      <b-nav-item href="/vue" v-on:click.prevent="navigateTo('/vue')"
        >Vue</b-nav-item
      >
      <b-nav-item href="/react" v-on:click.prevent="navigateTo('/react')"
        >React</b-nav-item
      >
    </b-nav>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
  props: {},
  methods: {
    navigateTo(url) {
      window.history.pushState(null, null, url);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
  text-align: right;
  display: block;
}
li {
  display: inline-block;
  margin: 0 10px;
}

#navbar ul {
  border-right: 1px solid #eee;
  padding-top: 76px;
  box-shadow: 0px 0px 5px #ccc;
}
</style>
