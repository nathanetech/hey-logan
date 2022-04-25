<script setup>
import {ref} from "vue"

const givingProof = ref(false);
const proveIt = () => {
  givingProof.value = !givingProof.value;
}
</script>

<template>
<div class="container" v-if="!givingProof">
  <h1 class="center">Hey Logan, I learned Vue</h1>
  <br />
  <br />
  <button @click="proveIt" class="btn center">Here's proof</button>
</div>
<div class="container" v-else>
  <iframe autoplay class="center" width="560" height="315" src="https://www.youtube.com/embed/dQw4w9WgXcQ?&autoplay=1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</template>

<style>
@import "@/assets/base.css";

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;

  font-weight: normal;
}

.container {
  text-align: center;
}

.btn {
  background: #1687b7;
  border: none;
  border-radius: 12px;
  font-weight: normal;
  font-size: 1.2rem;
  width: fit-content;
  padding: 0.5rem 1rem;
  cursor: pointer;
}

.center {
  margin-left: auto;
  margin-right: auto;
}

header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

a,
.green {
  text-decoration: none;
  color: hsla(160, 100%, 37%, 1);
  transition: 0.4s;
}

@media (hover: hover) {
  a:hover {
    background-color: hsla(160, 100%, 37%, 0.2);
  }
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  body {
    display: flex;
    place-items: center;
  }

  #app {
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding: 0 2rem;
  }

  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
