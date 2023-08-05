<script setup lang="ts">

let moved: Boolean = true;
function sidebarHandler() {
  let sideBar = document.getElementById("mobile-nav");
  sideBar.style.transform = "translateX(-260px)";
  if (moved) {
    sideBar.style.transform = "translateX(0px)";
    moved = false;
  } else {
    sideBar.style.transform = "translateX(-260px)";
    moved = true;
  }
}
</script>

<template>
    <div class="w-80 absolute sm:relative bg-ghostwhite shadow md:h-full flex-col justify-between hidden sm:flex">
      <div class="px-8">
        <div class="h-16 w-full flex items-center mt-4 place-content-center">
          <h1>BVG</h1>
        </div>
        <ul class="mt-8">
          <li class="flex w-full justify-between text-slate-600 hover:text-slate-500 cursor-pointer items-center mb-6">
            <div class="flex items-center">
              <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-grid" width="18" height="18" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                <path stroke="none" d="M0 0h24v24H0z"></path>
                <rect x="4" y="4" width="6" height="6" rx="1"></rect>
                <rect x="14" y="4" width="6" height="6" rx="1"></rect>
                <rect x="4" y="14" width="6" height="6" rx="1"></rect>
                <rect x="14" y="14" width="6" height="6" rx="1"></rect>
              </svg>
              <span class="text-sm ml-2">Backpack</span>
            </div>
            <div class="py-1 px-3 bg-slate-200 rounded text-slate-500 flex items-center justify-center text-xs">5</div>
          </li>
          <li class="flex w-full justify-between text-slate-600 hover:text-slate-600 cursor-pointer items-center mb-6">
            <div class="flex items-center">
              <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-puzzle" width="18" height="18" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                <path stroke="none" d="M0 0h24v24H0z"></path>
                <path d="M4 7h3a1 1 0 0 0 1 -1v-1a2 2 0 0 1 4 0v1a1 1 0 0 0 1 1h3a1 1 0 0 1 1 1v3a1 1 0 0 0 1 1h1a2 2 0 0 1 0 4h-1a1 1 0 0 0 -1 1v3a1 1 0 0 1 -1 1h-3a1 1 0 0 1 -1 -1v-1a2 2 0 0 0 -4 0v1a1 1 0 0 1 -1 1h-3a1 1 0 0 1 -1 -1v-3a1 1 0 0 1 1 -1h1a2 2 0 0 0 0 -4h-1a1 1 0 0 1 -1 -1v-3a1 1 0 0 1 1 -1"></path>
              </svg>
              <span class="text-sm ml-2">Explore</span>
            </div>
            <div class="py-1 px-3 bg-slate-200 rounded text-slate-500 flex items-center justify-center text-xs">8</div>
          </li>
          <li class="flex w-full justify-between text-slate-600 hover:text-slate-600 cursor-pointer items-center mb-6">
            <div class="flex items-center">
              <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-compass" width="18" height="18" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                <path stroke="none" d="M0 0h24v24H0z"></path>
                <polyline points="8 16 10 10 16 8 14 14 8 16"></polyline>
                <circle cx="12" cy="12" r="9"></circle>
              </svg>
              <span class="text-sm ml-2">Achievements</span>
            </div>
          </li>
          <li class="flex w-full justify-between text-slate-600 hover:text-slate-600 cursor-pointer items-center mb-6">
            <div class="flex items-center">
              <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-code" width="20" height="20" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                <path stroke="none" d="M0 0h24v24H0z"></path>
                <polyline points="7 8 3 12 7 16"></polyline>
                <polyline points="17 8 21 12 17 16"></polyline>
                <line x1="14" y1="4" x2="10" y2="20"></line>
              </svg>
              <span class="text-sm ml-2">Resources</span>
            </div>
          </li>
        </ul>
      </div>

    </div>
</template>

<style scoped>

</style>