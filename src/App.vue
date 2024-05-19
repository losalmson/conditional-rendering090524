<script setup lang="ts">
import Loader from './components/Loader.vue';
import HelloWorld from './components/HelloWorld.vue';
import { ref, onMounted } from 'vue';

const isLoading = ref(true);
const header = ref(false);

onMounted(() => {
  setTimeout(() => {
    isLoading.value = false;
    header.value = true;
  }, 3000);
});
</script>

<template>
  <Loader v-if="isLoading" />
  <HelloWorld v-else="header"/>
</template>

<style scoped>
</style>
