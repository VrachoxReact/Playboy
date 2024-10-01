<template>
  <section
    class="w-full py-8 md:py-12 bg-black text-white flex items-center justify-center"
  >
    <div class="container px-4 md:px-6 max-w-4xl mx-auto">
      <div class="flex flex-col items-center space-y-6 text-center">
        <h2
          class="text-2xl sm:text-3xl md:text-4xl lg:text-5xl font-bold tracking-tighter"
        >
          Special Offer: 20% Off Your First Rental
        </h2>
        <p
          class="max-w-[600px] text-sm sm:text-base md:text-lg lg:text-xl text-white/90"
        >
          New customers get 20% off their first rental. Don't miss out on this
          limited-time offer!
        </p>
        <router-link
          to="/signup"
          class="inline-flex items-center justify-center rounded-md text-sm font-medium ring-offset-background transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 disabled:pointer-events-none disabled:opacity-50 bg-white text-black hover:bg-white/90 h-10 px-4 py-2 md:h-11 md:px-8"
        >
          Claim Your Discount
        </router-link>
      </div>
    </div>
  </section>
</template>

<script setup>
// No setup logic needed for this component
</script>
