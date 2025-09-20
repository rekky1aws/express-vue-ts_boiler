<script setup lang="ts">
import { ref } from "vue";

const baseURL = __API_PATH__;

const isLoading = ref(false);
const message = ref("");

async function fetchAPI () {
  try {
    isLoading.value = true;

    const response = await fetch(baseURL);

    const data = await response.json();

    message.value = data.message;
  } catch (err) {
    message.value = "Error fetching data";
    console.error(err);
  } finally {
    isLoading.value = false;
  }
}
</script>

<template>
 <button @click="fetchAPI">Fetch</button>

  <p v-if="isLoading">Loading...</p>

  <p v-else-if="message">{{ message }}</p>
</template>