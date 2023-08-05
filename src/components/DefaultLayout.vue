<script setup lang="ts">
const today = new Date()
const localeDateString = new Date().toLocaleDateString('en-ZA', {
  weekday: "long",
  year: "numeric",
  month: "short",
  day: "numeric"
});
</script>

<template>
  <div class="flex flex-no-wrap bg-ghostwhite h-screen">
    <!--    <SidebarLayout/>-->
    <div class="container mx-auto py-10 h-64 md:w-4/5 w-11/12 px-6">
      <div class="">
        <h1 v-if="today.getHours() < 12">Good Morning</h1>
        <h1 v-else-if="today.getHours() >= 12 && today.getHours() < 18">Good Afternoon</h1>
        <h1 v-else-if="today.getHours() >= 18 && today.getHours() < 21">Good Evening</h1>
        <h1 v-else>Good Night</h1>
        <h3 class="-mt-4 mb-4">{{ localeDateString }}</h3>
      </div>
      <Calendar/>
      <div class=" mt-4 w-full h-80 rounded border-dashed border-2 border-slate-300">
        <div class="wrapper">

        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  max-width: 1100px;
  margin: 0 auto;
  padding: 2rem;
  font-weight: normal;
  max-height: 90%;
}
</style>