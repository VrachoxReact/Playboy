<template>
  <footer class="w-full border-t bg-blue-800 text-white">
    <div
      class="container mx-auto flex flex-col items-center justify-center space-y-6 py-10 md:py-8"
    >
      <div class="flex flex-col items-center gap-4">
        <img
          :src="logo"
          width="48"
          height="48"
          alt="Zeko Rent logo"
          class="rounded-lg"
        />
        <p class="text-center text-sm leading-loose text-blue-200">
          © 2024 Zeko Rent. All rights reserved.
        </p>
      </div>
      <nav class="flex flex-wrap justify-center gap-4 sm:gap-6">
        <router-link
          class="text-sm font-medium hover:text-blue-300 transition duration-300"
          to="/"
        >
          Home
        </router-link>
        <router-link
          class="text-sm font-medium hover:text-blue-300 transition duration-300"
          to="/services"
        >
          Services
        </router-link>
        <router-link
          class="text-sm font-medium hover:text-blue-300 transition duration-300"
          to="/about"
        >
          About
        </router-link>
        <router-link
          class="text-sm font-medium hover:text-blue-300 transition duration-300"
          to="/contact"
        >
          Contact
        </router-link>
      </nav>
      <div class="flex gap-6">
        <a
          href="#"
          aria-label="Facebook"
          class="text-blue-300 hover:text-white transition duration-300"
        >
          <Facebook class="h-6 w-6" />
        </a>
        <a
          href="#"
          aria-label="Instagram"
          class="text-blue-300 hover:text-white transition duration-300"
        >
          <Instagram class="h-6 w-6" />
        </a>
        <a
          href="#"
          aria-label="Twitter"
          class="text-blue-300 hover:text-white transition duration-300"
        >
          <Twitter class="h-6 w-6" />
        </a>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { Facebook, Instagram, Twitter } from "lucide-vue-next";
import logo from "../assets/logo.png";
</script>
