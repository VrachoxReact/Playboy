<template>
  <section class="w-full py-12 md:py-24 lg:py-32 bg-blue-50">
    <div class="container mx-auto px-4 md:px-6">
      <h2 class="text-3xl font-bold text-center text-blue-800 mb-12">
        Our Services
      </h2>
      <div :class="gridClass">
        <ServiceCard
          v-for="(service, index) in limitedServices"
          :key="index"
          v-bind="service"
          class="bg-white rounded-lg shadow-lg hover:shadow-xl transition duration-300 overflow-hidden"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
import { computed } from "vue";
import ServiceCard from "./ServiceCard.vue";

const props = defineProps({
  gridCols: {
    type: Number,
    default: 3,
  },
  maxServices: {
    type: Number,
    default: Infinity,
  },
});

const services = [
  {
    id: "car-rental",
    title: "Car Rental",
    description: "Wide range of vehicles for any occasion.",
    image: "car.jpg",
  },
  {
    id: "equipment-rental",
    title: "Equipment Rental",
    description: "Tools and machinery for your projects.",
    image: "equipment.jpg",
  },
  {
    id: "party-supplies",
    title: "Party Supplies",
    description: "Everything you need for a perfect event.",
    image: "party.jpg",
  },
  {
    id: "bike-rental",
    title: "Bike Rental",
    description: "Explore the city on two wheels.",
    image: "bike.jpg",
  },
  {
    id: "camera-gear",
    title: "Camera Gear",
    description: "Professional equipment for photographers.",
    image: "camera.jpg",
  },
  {
    id: "outdoor-gear",
    title: "Outdoor Gear",
    description: "Camping and hiking equipment for adventures.",
    image: "outdoor.jpg",
  },
  {
    id: "sports-equipment",
    title: "Sports Equipment",
    description: "Gear for various sports activities.",
    image: "sports.jpg",
  },
  {
    id: "formal-wear",
    title: "Formal Wear",
    description: "Suits and dresses for special occasions.",
    image: "formalwear.jpg",
  },
  {
    id: "home-appliances",
    title: "Home Appliances",
    description: "Short-term appliance rentals for your home.",
    image: "appliances.jpg",
  },
];

const gridClass = computed(() => {
  return `grid grid-cols-1 md:grid-cols-2 lg:grid-cols-${props.gridCols} gap-6`;
});

const limitedServices = computed(() => {
  return services.slice(0, props.maxServices);
});
</script>
