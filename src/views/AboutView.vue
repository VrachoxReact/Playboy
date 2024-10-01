<template>
  <div class="about-page bg-gray-100 min-h-screen">
    <div class="container mx-auto px-4 py-16">
      <h1 class="text-4xl font-bold text-center mb-8 text-indigo-600">
        About Zeko
      </h1>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
        <div class="about-content">
          <h2 class="text-2xl font-semibold mb-4 text-gray-800">Our Mission</h2>
          <p class="text-gray-600 mb-6">
            At Zeko, we're passionate about revolutionizing the way businesses
            handle their logistics. Our mission is to provide innovative,
            efficient, and sustainable solutions that empower companies to
            streamline their operations and focus on what they do best.
          </p>
          <h2 class="text-2xl font-semibold mb-4 text-gray-800">
            Why Choose Us?
          </h2>
          <ul class="list-disc list-inside text-gray-600 mb-6">
            <li>Cutting-edge technology integration</li>
            <li>Eco-friendly practices</li>
            <li>Customized solutions for every business</li>
            <li>24/7 customer support</li>
            <li>Proven track record of success</li>
          </ul>
        </div>

        <div class="about-image">
          <img
            src="https://picsum.photos/800/600"
            alt="Zeko Team"
            class="rounded-lg shadow-md w-full h-auto"
          />
        </div>
      </div>

      <div class="mt-16">
        <h2 class="text-2xl font-semibold mb-6 text-center text-gray-800">
          Our Values
        </h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div class="bg-white p-6 rounded-lg shadow-md">
            <h3 class="text-xl font-semibold mb-2 text-indigo-600">
              Innovation
            </h3>
            <p class="text-gray-600">
              We constantly push the boundaries to bring you the latest in
              logistics technology.
            </p>
          </div>
          <div class="bg-white p-6 rounded-lg shadow-md">
            <h3 class="text-xl font-semibold mb-2 text-indigo-600">
              Sustainability
            </h3>
            <p class="text-gray-600">
              We're committed to reducing our environmental impact and promoting
              green practices.
            </p>
          </div>
          <div class="bg-white p-6 rounded-lg shadow-md">
            <h3 class="text-xl font-semibold mb-2 text-indigo-600">
              Customer-Centric
            </h3>
            <p class="text-gray-600">
              Your success is our success. We tailor our solutions to meet your
              unique needs.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
// No additional script needed for this component
</script>
