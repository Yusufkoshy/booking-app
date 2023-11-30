<template>
  <div class="relative form__picker">
    <form
      class="bg-white py-5 rounded-xl shadow-lg flex items-center justify-between"
    >
      <i class="material-icons">location_on</i>
      <input
        class="border-0 rounded-lg p-2 bg-zinc-200 outline-none"
        placeholder="where are you going?"
        list="destinations"
        name="browser"
        id="browser"
      />
      <datalist id="destinations">
        <option v-for="destination in destinations" :key="destination">
          {{ destination.city_name }}
        </option>
      </datalist>
      <div class="input-icons flex items-center justify-center">
        <i class="material-icons color-zinc-200">calendar_month</i>
        <input
          placeholder="Check out date"
          class="bg-zinc-200 rounded-lg p-2"
          type="text"
          onfocus="(this.type='date')"
          onblur="(this.type='text')"
          id="date"
        />
      </div>
      <div class="input-icons flex items-center justify-center">
        <i class="material-icons">calendar_month</i>
        <input
          placeholder="Check out date"
          class="bg-zinc-200 rounded-lg p-2"
          type="text"
          onfocus="(this.type='date')"
          onblur="(this.type='text')"
          id="date"
        />
      </div>
      <div class="input-icons flex items-center justify-center">
        <i class="material-icons">person</i>
        <input
          class="bg-zinc-200 rounded-lg p-2"
          type="text"
          placeholder="Guests"
        />
      </div>
      <div class="input-icons flex items-center justify-center">
        <i class="material-icons">bedroom_parent</i>
        <input
          class="bg-zinc-200 rounded-lg p-2"
          type="text"
          placeholder="Rooms"
        />
      </div>
    </form>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";

var destinations = ref([]);
const getDestinations = async () => {
  const url = `https://booking-com15.p.rapidapi.com/api/v1/hotels/searchDestination?query=man`;
  const options = {
    method: "GET",
    headers: {
      "X-RapidAPI-Key": "fe815d0724msh2581e24cb3b3e75p1120e3jsn43cc20cd33f4",
      "X-RapidAPI-Host": "booking-com15.p.rapidapi.com",
    },
  };

  try {
    const response = await fetch(url, options);
    const results = await response.json();
    destinations.value = results.data;
    console.log(destinations);
  } catch (error) {
    console.error(error);
  }
};

onMounted(() => {
  getDestinations();
});
</script>

<style lang="scss" scoped>
input::-webkit-calendar-picker-indicator {
  opacity: 100;
  color: dimgrey;
}
.form__picker {
  top: 26em;
}
</style>
