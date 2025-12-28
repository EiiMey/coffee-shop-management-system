<template>
  <div class="ml-64 min-h-screen bg-gray-100">
    <Navbar />

    <div class="p-6">
      <div class="grid grid-cols-1 md:grid-cols-4 gap-6">
        <StatCard title="Users" value="1,245" />
        <StatCard title="Revenue" value="$12,500" />
        <StatCard title="Orders" value="320" />
        <StatCard title="Growth" value="+12%" />
      </div>

      <div class="mt-8 bg-white p-6 rounded-lg shadow">
        <h2 class="text-lg font-semibold mb-4">Recent Activity</h2>
        <p class="text-gray-500">Dashboard content goes here...</p>
      </div>
    </div>
  </div>
</template>

<script setup>
import Navbar from '../components/Navbar.vue'
import StatCard from '../components/StatCard.vue'
</script>
