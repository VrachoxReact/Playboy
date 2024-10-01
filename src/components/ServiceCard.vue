<template>
  <div
    class="flex flex-col justify-between bg-white rounded-lg shadow-md overflow-hidden"
  >
    <div class="p-4">
      <img
        :src="`/placeholder.svg?height=200&width=300&text=${image}`"
        :alt="title"
        width="300"
        height="200"
        class="w-full h-48 object-cover rounded-md mb-4"
      />
      <h3 class="text-xl font-semibold mb-2">{{ title }}</h3>
      <p class="text-gray-600">{{ description }}</p>
    </div>
    <div class="p-4 bg-gray-50">
      <router-link
        :to="`/services/${id}`"
        class="inline-block px-4 py-2 bg-blue-600 text-white rounded hover:bg-blue-700 transition-colors"
      >
        See More
      </router-link>
    </div>
  </div>
</template>

<script setup>
defineProps({
  id: String,
  title: String,
  description: String,
  image: String,
});
</script>
