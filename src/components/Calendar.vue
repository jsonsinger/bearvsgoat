<script setup lang="ts">
let current = new Date();
let days = [];
// Starting Monday not Sunday
let sundayStart = 0;
let mondayStart = 1;

let startOfMonth = new Date(current.getFullYear(), current.getMonth(), 1);
let endOfMonth = new Date(current.getFullYear(), current.getMonth() + 1, 0);

current.setDate((current.getDate() - current.getDay() + mondayStart));
for (let i = startOfMonth.getDate(); i < endOfMonth.getDate(); i++) {
  days.push(new Date(current));
  current.setDate(current.getDate() + 1);
}
</script>

<template>
  <div class="w-full h-16 px-2 rounded border-dashed border-opacity-25 border-2 border-slate-300">
    <section class="content">
      <div class="scrolling-wrapper">
        <div class="card" v-for="day in days">
          <div>
            <span class="flex flex-col justify-center items-center text-gray-500">
              <small>{{ day.toLocaleDateString('en-ZA', {weekday: "short"}) }} </small>
              {{ day.getDate() }}
            </span>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>

:root {
  --days: 7;
}

@property --days {
  syntax: "<number>";
  initial-value: 7;
  inherits: true;
}

.scrolling-wrapper {
  overflow-x: scroll;
  overflow-y: hidden;
  white-space: nowrap;

  .card {
    display: inline-flex;
    justify-content: center;
    align-items: center;
  }
}

.card {
  width: calc(100% / var(--days));
  height: 60px;
  background: ghostwhite;

  :hover span {
    padding-left: 6px;
    padding-right: 6px;
    margin: 2px;
    border: 2px solid lightslategray;
    border-radius: 20%;
    cursor: pointer;
  }
}

.scrolling-wrapper {
  height: 80px;
  margin-bottom: 20px;
  width: 100%;
  -webkit-overflow-scrolling: touch;
  touch-action: pan-x;

  &::-webkit-scrollbar {
    display: none;
  }
}

@media (min-width: 1024px) {
  .card {
    --days: 21;
  }
}
</style>