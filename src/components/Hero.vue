<template>
  <section
    class="w-full py-12 md:py-24 lg:py-32 xl:py-48 bg-gradient-to-br from-blue-500 to-blue-700"
  >
    <div class="container px-4 md:px-6">
      <div
        class="grid gap-6 lg:grid-cols-[1fr_400px] lg:gap-12 xl:grid-cols-[1fr_600px]"
      >
        <div class="flex flex-col justify-center space-y-4">
          <div class="space-y-2">
            <h1
              class="text-3xl font-bold tracking-tighter sm:text-5xl xl:text-6xl/none text-white"
            >
              Rent Anything, Anytime
            </h1>
            <p class="max-w-[600px] text-blue-100 md:text-xl">
              Zeko Rent offers a wide range of rental services. From equipment
              to vehicles, we've got you covered for all your temporary needs.
            </p>
          </div>
          <div class="flex flex-col gap-2 min-[400px]:flex-row">
            <button
              class="px-6 py-3 text-blue-700 bg-white rounded-full hover:bg-blue-50 focus:outline-none focus:ring-2 focus:ring-white focus:ring-opacity-50 transition duration-300 shadow-lg"
            >
              <router-link
                to="/services"
                class="text-blue-700 no-underline font-semibold"
              >
                Start Renting Now
              </router-link>
            </button>
          </div>
        </div>
        <img
          alt="Rental items collage"
          class="mx-auto aspect-video overflow-hidden rounded-xl object-cover object-center sm:w-full lg:order-last shadow-xl"
          height="550"
          src="https://placehold.co/550x550"
          width="550"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
// No imports needed
</script>
