<template>
  <nav
    class="w-full sticky bg-white top-0 shadow-sm flex flex-col sm:flex-row items-center py-6 px-5"
  >
    <div class="flex font-bold">
      <img src="./assets/bxs-plane-alt 1.svg" alt="plane logo" />
      <span>my Dream Place</span>
    </div>
    <div class="m-auto">
      <router-link class="p-5" :to="{ name: 'home' }">Home</router-link>
      <router-link class="p-5" :to="{ name: 'home' }">Discover</router-link>
      <router-link class="p-5" :to="{ name: 'home' }">Activities</router-link>
      <router-link class="p-5" :to="{ name: 'home' }">About</router-link>
      <router-link class="p-5" :to="{ name: 'home' }">Contact</router-link>
    </div>
    <div class="ml-auto">
      <router-link :to="{ name: 'home' }"
        ><button class="bg-sky-600 text-white p-2 rounded-md">
          Register
        </button></router-link
      >
    </div>
  </nav>
  <router-view />
</template>
<script setup></script>

<style lang="scss">
#app {
  font-family: sans-serif;
  padding: 0px;
  margin: 0px;
  box-sizing: border-box;
}
</style>
