<template>
  <div class="space-x-4 mb-10" id="nav">
    <router-link class="p-2" to="/">Home</router-link> 
    <span>|</span>
    <router-link class="p-2" :to="{ name: 'About' }">About</router-link>
    <span>|</span>
    <router-link class="p-2" :to="{ name: 'Jobs' }">Jobs</router-link>
  </div>
  <router-view />
</template>

<script>
export default {};
</script>

<style scoped>
#nav a.router-link-active , .router-link-exact-active{
  color: white;
  border-radius: 11px;
  background-color: red;
}
</style>