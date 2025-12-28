<template>
  <div class="bg-white p-6 rounded-lg shadow">
    <h3 class="text-gray-500 text-sm">{{ title }}</h3>
    <p class="text-2xl font-bold mt-2">{{ value }}</p>
  </div>
</template>

<script setup>
defineProps({
  title: String,
  value: String
})
</script>
