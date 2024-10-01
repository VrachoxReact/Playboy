<template>
  <div class="services-view bg-blue-50 min-h-screen">
    <div class="container mx-auto px-4 py-12">
      <h1 class="text-4xl font-bold text-center text-blue-800 mb-8">
        Our Services
      </h1>
      <p class="text-center text-blue-600 max-w-2xl mx-auto mb-12">
        Discover our wide range of rental services designed to meet all your
        needs. From vehicles to equipment, we've got you covered.
      </p>
      <ServicesSection :gridCols="3" :maxServices="9" />
    </div>
  </div>
</template>

<script setup>
import ServicesSection from "@/components/ServicesSection.vue";
</script>
