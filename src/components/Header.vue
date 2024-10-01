<template>
  <header class="bg-blue-600 shadow-md">
    <div class="container mx-auto px-4 py-4 flex items-center justify-between">
      <div class="flex items-center">
        <img :src="logo" alt="Zeko Rent Logo" class="h-12 w-12 mr-3" />
        <span class="text-xl font-bold text-white">Zeko Rent</span>
      </div>

      <div class="hidden md:flex items-center space-x-4">
        <a
          href="https://instagram.com"
          class="text-white hover:text-blue-200 transition duration-300"
        >
          <Instagram :size="24" />
          <span class="sr-only">Instagram</span>
        </a>
        <a
          href="https://facebook.com"
          class="text-white hover:text-blue-200 transition duration-300"
        >
          <Facebook :size="24" />
          <span class="sr-only">Facebook</span>
        </a>
      </div>
      <nav class="hidden md:flex space-x-4">
        <router-link
          to="/"
          class="text-white hover:text-blue-200 transition duration-300"
          >Home</router-link
        >
        <router-link
          to="/services"
          class="text-white hover:text-blue-200 transition duration-300"
          >Services</router-link
        >
        <router-link
          to="/about"
          class="text-white hover:text-blue-200 transition duration-300"
          >About</router-link
        >
        <router-link
          to="/contact"
          class="text-white hover:text-blue-200 transition duration-300"
          >Contact</router-link
        >
      </nav>
      <button class="md:hidden text-white" @click="toggleMenu">
        <X v-if="isMenuOpen" :size="24" />
        <Menu v-else :size="24" />
      </button>
    </div>
    <div v-if="isMenuOpen" class="md:hidden">
      <nav class="flex flex-col items-center py-4 bg-blue-700">
        <router-link
          to="/"
          class="py-2 text-white hover:text-blue-200 transition duration-300"
          >Home</router-link
        >
        <router-link
          to="/services"
          class="py-2 text-white hover:text-blue-200 transition duration-300"
          >Services</router-link
        >
        <router-link
          to="/about"
          class="py-2 text-white hover:text-blue-200 transition duration-300"
          >About</router-link
        >
        <router-link
          to="/contact"
          class="py-2 text-white hover:text-blue-200 transition duration-300"
          >Contact</router-link
        >
      </nav>
      <div class="flex justify-center space-x-4 py-4 bg-blue-700">
        <a
          href="https://instagram.com"
          class="text-white hover:text-blue-200 transition duration-300"
        >
          <Instagram :size="24" />
          <span class="sr-only">Instagram</span>
        </a>
        <a
          href="https://facebook.com"
          class="text-white hover:text-blue-200 transition duration-300"
        >
          <Facebook :size="24" />
          <span class="sr-only">Facebook</span>
        </a>
      </div>
    </div>
  </header>
</template>

<script setup>
import { ref } from "vue";
import { Menu, X, Instagram, Facebook } from "lucide-vue-next";
import logo from "../assets/logo.png";

const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};
</script>
