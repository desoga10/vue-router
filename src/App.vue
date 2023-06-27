<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />
    <button @click="redirect">Redirect</button>
    <button @click="back">Go Back</button>
    <button @click="forward">Go Forward</button>
    <div class="wrapper">
      <HelloWorld msg="You did it!" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink :to="{ name: 'about' }">About</RouterLink>
        <RouterLink :to="{ name: 'jobs' }">Jobs</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<script>
export default {
  methods: {
    redirect() {
      this.$router.push({ name: 'about' })
    },
    back() {
      this.$router.go(-1)
    },
    forward() {
      this.$router.go(1)
    }
  }
}
</script>


<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
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

button {
  display: block;
  margin: 2 auto 2rem;
  padding: 0.5rem 1rem;
  border: 1px solid var(--color-border);
  border-radius: 0.25rem;
  background-color: transparent;
  color: var(--color-text);
  font-size: 1rem;
  cursor: pointer;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
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
