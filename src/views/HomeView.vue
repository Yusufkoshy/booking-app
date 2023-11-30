<template>
  <div class="container">
    <header class="home">
      <div class="my-5">
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
          <FormPicker :destinations="Object" />
        </div>
      </div>
    </header>
    <div class="covid__warning my-12 mx-5 p-3 rounded-lg bg-yellow-200">
      <span
        >check the latest COVID-19 restrictions before you travel.
        <a href="#" class="text-sky-700">Learn more</a></span
      >
    </div>
    <h1 class="text-3xl font-bold mb-2">Enjoy your dream vacation</h1>
    <p>
      Plan and book our perfect trip with expert advice, travel tips,
      destination information and <br />
      inspiration from us
    </p>
    <section class="countries flex items-center justify-between my-10">
      <div class="pictures__details">
        <img src="../assets/Rectangle 8.png" alt="Australia" />
        <div class="mt-2">
          <span class="pt-2 font-semibold">Australia</span>
          <p>2246 properties</p>
        </div>
      </div>
      <div>
        <img src="../assets/Rectangle 9.png" alt="Japan" />
        <div class="mt-2">
          <span class="pt-2 font-semibold">Japan</span>
          <p>1278 properties</p>
        </div>
      </div>
      <div>
        <img src="../assets/Rectangle 10.png" alt="New Zealand" />
        <div class="mt-2">
          <span class="pt-2 font-semibold">New Zealand</span>
          <p>480 properties</p>
        </div>
      </div>
      <div>
        <img src="../assets/Rectangle 11.png" alt="Greece" />
        <div class="mt-2">
          <span class="pt-2 font-semibold">Greece</span>
          <p>320 properties</p>
        </div>
      </div>
    </section>
    <h1 class="text-3xl font-bold mb-2">Get inspiration for your next trip</h1>
  </div>
</template>

<script>
import FormPicker from "@/components/FormPicker.vue";
export default {
  components: {
    FormPicker,
  },
  props: "destinations",
};
</script>

<style lang="scss">
.header__div {
  background-image: url(../assets/Rectangle\ 2.png);
  background-size: cover;
  background-repeat: no-repeat;
  padding-bottom: 24em;
}
</style>
