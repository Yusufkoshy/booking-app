<template>
  <header class="home">
    <div class="mx-10 my-5">
      <div class="header__div w-full rounded-lg px-5">
        <div class="text-center relative top-40">
          <h1 class="text-white text-2xl font-bold pt-11">
            Enjoy Your Dream Vacation
          </h1>
          <h2 class="text-white text-lg leading-10 p-5">
            Plan and book our perfect trip with expert advice, travel tips,
            destination information and inspiration from us
          </h2>
        </div>
        <FormPicker />
      </div>
    </div>
  </header>
</template>

<script setup>
import FormPicker from "@/components/FormPicker.vue";
</script>

<style lang="scss">
.header__div {
  background-image: url(../assets/Rectangle\ 2.png);
  background-size: cover;
  background-repeat: no-repeat;
  padding-bottom: 24em;
}
</style>
