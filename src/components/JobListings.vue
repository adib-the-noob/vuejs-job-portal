<script setup>
import jobData from '@/assets/jobs.json';
import { ref } from "vue";

const jobs = ref(jobData);
</script>

<template>
  <section class="bg-gradient-to-br from-[#F2EFE7] to-[#9ACBD0] px-4 py-12">
    <h2 class="text-3xl font-bold text-[#006A71] text-center py-8 tracking-tight">Explore Job Opportunities</h2>
    <div class="container-xl lg:container mx-auto">
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div
            v-for="job in jobs"
            :key="job.id"
            class="bg-white rounded-xl shadow-lg p-6 hover:shadow-xl transition-all duration-300 transform hover:-translate-y-1"
        >
          <div class="flex flex-col space-y-5">
            <p class="text-[#48A6A7] text-sm uppercase font-medium tracking-wide">{{ job.type || 'Full-Time' }}</p>
            <h2 class="text-2xl font-bold text-[#006A71] leading-tight">{{ job.title }}</h2>
            <p class="text-[#006A71] text-base line-clamp-3 leading-relaxed">{{ job.description }}</p>
            <p class="text-[#006A71] text-lg font-semibold">{{ job.salary }} / Year</p>
            <p class="text-[#48A6A7] text-sm font-medium flex items-center">
              <svg class="w-4 h-4 mr-1" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path>
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path>
              </svg>
              {{ job.location }}
            </p>
            <hr class="border-gray-200 my-4">
            <a :href="'/jobs/' + job.id">
              <button
                  class="bg-[#48A6A7] hover:bg-[#006A71] text-white py-3 px-4 rounded-lg text-base font-medium w-full transition duration-300 ease-in-out transform hover:scale-105"
              >
                Discover More
              </button>
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* Additional custom styles can go here if needed */
</style>