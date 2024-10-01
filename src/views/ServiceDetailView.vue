<template>
  <div class="service-detail-view bg-blue-50 min-h-screen py-12">
    <div class="container mx-auto px-4">
      <div v-if="service" class="bg-white rounded-lg shadow-lg p-8">
        <h1 class="text-4xl font-bold text-blue-800 mb-6">
          {{ service.title }}
        </h1>
        <img
          :src="`/placeholder.svg?height=400&width=800&text=${service.image}`"
          :alt="service.title"
          class="w-full h-64 object-cover rounded-lg mb-6"
        />
        <p class="text-xl text-gray-700 mb-8">{{ service.description }}</p>
        <router-link
          to="/services"
          class="inline-block px-6 py-3 bg-blue-600 text-white rounded-full hover:bg-blue-700 transition-colors"
        >
          Back to Services
        </router-link>
      </div>
      <div v-else class="text-center text-2xl text-gray-700">
        Service not found
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";
import { useRoute } from "vue-router";

const route = useRoute();
const service = ref(null);

const services = [
  {
    id: "car-rental",
    title: "Car Rental",
    description:
      "Wide range of vehicles for any occasion. Whether you need a compact car for a quick city trip or a spacious SUV for a family vacation, we have the perfect vehicle for you. Our fleet includes economy cars, luxury vehicles, and everything in between.",
    image: "car.jpg",
  },
  {
    id: "equipment-rental",
    title: "Equipment Rental",
    description:
      "Tools and machinery for your projects. From power tools to heavy machinery, we offer a comprehensive range of equipment to help you complete your tasks efficiently and professionally.",
    image: "equipment.jpg",
  },
  {
    id: "party-supplies",
    title: "Party Supplies",
    description:
      "Everything you need for a perfect event. From decorations to tableware, we provide a wide selection of party supplies to make your celebration memorable and hassle-free.",
    image: "party.jpg",
  },
  {
    id: "bike-rental",
    title: "Bike Rental",
    description:
      "Explore the city on two wheels. Our bike rental service offers a variety of bicycles for all ages and skill levels, perfect for sightseeing or a leisurely ride through the park.",
    image: "bike.jpg",
  },
  {
    id: "camera-gear",
    title: "Camera Gear",
    description:
      "Professional equipment for photographers. From DSLR cameras to lenses and lighting equipment, we have everything you need to capture your perfect shot.",
    image: "camera.jpg",
  },
  {
    id: "outdoor-gear",
    title: "Outdoor Gear",
    description:
      "Camping and hiking equipment for adventures. Get ready for your next outdoor expedition with our high-quality tents, sleeping bags, backpacks, and more.",
    image: "outdoor.jpg",
  },
  {
    id: "sports-equipment",
    title: "Sports Equipment",
    description:
      "Gear for various sports activities. Whether you're into team sports or individual activities, we have the equipment you need to stay active and have fun.",
    image: "sports.jpg",
  },
  {
    id: "formal-wear",
    title: "Formal Wear",
    description:
      "Suits and dresses for special occasions. Look your best at weddings, galas, or business events with our selection of elegant formal wear for men and women.",
    image: "formalwear.jpg",
  },
  {
    id: "home-appliances",
    title: "Home Appliances",
    description:
      "Short-term appliance rentals for your home. From refrigerators to washing machines, we offer a range of home appliances to make your life easier during temporary situations.",
    image: "appliances.jpg",
  },
];

onMounted(() => {
  const serviceId = route.params.id;
  service.value = services.find((s) => s.id === serviceId);
});
</script>
