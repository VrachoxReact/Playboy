<template>
  <div class="contact-view bg-gray-100 py-12 px-4 sm:px-6 lg:px-8">
    <div class="max-w-7xl mx-auto">
      <h1 class="text-4xl font-bold text-center text-blue-900 mb-12">
        Contact Us
      </h1>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
        <div class="bg-white shadow-lg rounded-lg p-8">
          <h2 class="text-2xl font-semibold text-blue-800 mb-6">
            Get in Touch
          </h2>
          <form @submit.prevent="submitForm" class="space-y-6">
            <div>
              <label for="name" class="block text-sm font-medium text-gray-700"
                >Name</label
              >
              <input
                type="text"
                id="name"
                v-model="form.name"
                required
                class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-blue-500 focus:ring-blue-500"
              />
            </div>
            <div>
              <label for="email" class="block text-sm font-medium text-gray-700"
                >Email</label
              >
              <input
                type="email"
                id="email"
                v-model="form.email"
                required
                class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-blue-500 focus:ring-blue-500"
              />
            </div>
            <div>
              <label
                for="message"
                class="block text-sm font-medium text-gray-700"
                >Message</label
              >
              <textarea
                id="message"
                v-model="form.message"
                rows="4"
                required
                class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-blue-500 focus:ring-blue-500"
              ></textarea>
            </div>
            <button
              type="submit"
              class="w-full bg-blue-600 text-white py-2 px-4 rounded-md hover:bg-blue-700 transition duration-300"
            >
              Send Message
            </button>
          </form>
        </div>
        <div class="space-y-8">
          <div class="bg-white shadow-lg rounded-lg p-8">
            <h2 class="text-2xl font-semibold text-blue-800 mb-6">
              Contact Information
            </h2>
            <div class="space-y-4">
              <div class="flex items-center">
                <MapPin class="text-blue-600 mr-3" />
                <span>Ilica 242, 10000 Zagreb, Croatia</span>
              </div>
              <div class="flex items-center">
                <Phone class="text-blue-600 mr-3" />
                <span>+385 1 2345 678</span>
              </div>
              <div class="flex items-center">
                <Mail class="text-blue-600 mr-3" />
                <span>info@zekorent.com</span>
              </div>
            </div>
          </div>
          <div class="bg-white shadow-lg rounded-lg p-8">
            <h2 class="text-2xl font-semibold text-blue-800 mb-6">Find Us</h2>
            <div class="aspect-w-16 aspect-h-9">
              <iframe
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2781.7974916102924!2d15.950361315785592!3d45.81325307910645!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x4765d1dc8a243b3f%3A0x7f0d8e2d3a8a9c0c!2sIlica%20242%2C%2010000%2C%20Zagreb%2C%20Croatia!5e0!3m2!1sen!2sus!4v1621234567890!5m2!1sen!2sus"
                width="100%"
                height="100%"
                style="border: 0"
                allowfullscreen=""
                loading="lazy"
              ></iframe>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { MapPin, Phone, Mail } from "lucide-vue-next";

const form = ref({
  name: "",
  email: "",
  message: "",
});

function submitForm() {
  // Here you would typically send the form data to your backend
  console.log("Form submitted:", form.value);
  // Reset form after submission
  form.value = { name: "", email: "", message: "" };
  // You might want to show a success message to the user here
}
</script>
