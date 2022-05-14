<template>
  <div class="text-center space-y-4">
    <h2 class="text-xl font-bold">Jobs Page</h2>
    <ul class="space-y-4">
      <li v-for="(job,index) in jobs" :key="index" class="bg-gray-200 p-4 px-20 text-gray-700 rounded-lg cursor-pointer hover:scale-105 duration-300 hover:bg-gray-300">
      <router-link :to="{ name: 'JobDetails', params: { id:job.id } }" > {{ job.title }} </router-link>
      </li>
    </ul>
  </div>
</template>

<script>
import { reactive, toRefs } from "vue";

export default {
  setup() {
    const jobs = reactive([
      {
        id: 0,
        title: "Front end developer",
      },
      {
        id: 1,
        title: "Back end developer",
      },
      {
        id: 2,
        title: "QA developer",
      },
    ]);

    return {
      jobs
    };
   
  },
};
</script>

<style>
</style>