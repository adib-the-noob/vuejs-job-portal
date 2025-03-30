<script setup>
import Card from "@/components/Card.vue";
</script>

<template>
  <section class="py-4">
    <div class="container-xl lg:container m-auto">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-4 p-4 rounded-lg">
        <Card>
          <h2 class="text-2xl font-bold text-[#006A71]">For Developers</h2>
          <p class="mt-2 mb-4 text-[#006A71]">
            Browse our Vue jobs and start your career today
          </p>
          <a
              href="jobs.html"
              class="inline-block bg-[#006A71] text-[#F2EFE7] rounded-lg px-4 py-2 hover:bg-[#48A6A7]"
          >
            Browse Jobs
          </a>
        </Card>

        <Card bg="bg-[#9ACBD0]">
          <h2 class="text-2xl font-bold text-[#006A71]">For Employers</h2>
          <p class="mt-2 mb-4 text-[#006A71]">
            List your job to find the perfect developer for the role
          </p>
          <a
              href="add-job.html"
              class="inline-block bg-[#006A71] text-[#F2EFE7] rounded-lg px-4 py-2 hover:bg-[#48A6A7]"
          >
            Add Job
          </a>
        </Card>
      </div>
    </div>
  </section>
</template>

<style scoped>

</style>