<template>
  <div>
    <ul id="destinations">
      <li v-for="destination in destinations" :key="destination">
        {{ destination.city_name }}
      </li>
    </ul>
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
      "X-RapidAPI-Key": "fd35c9d750mshcb7b59c576d21b7p144f86jsn4807638c8897",
      "X-RapidAPI-Host": "booking-com15.p.rapidapi.com",
    },
  };

  try {
    const response = await fetch(url, options);
    const results = await response.json();
    destinations = results.data;
    console.log(destinations);
  } catch (error) {
    console.error(error);
  }
};

onMounted(() => {
  getDestinations();
});
</script>

<style lang="scss" scoped></style>
