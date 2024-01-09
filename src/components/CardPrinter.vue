<template>
    <div class="flex justify-center items-center min-h-screen  bg-gray-300 ">
    <div class="max-w-2xl mx-auto bg-white p-4 shadow rounded-lg flex">
      <div class="flex flex-col w-1/2 items-center">
        <div class="flex items-center mb-7">
  <v-icon size="30" class="icon-background mr-4">mdi-printer</v-icon> 
          <div class="flex-grow">
            <h2 class="text-xl font-bold text-gray-800 truncate mb-2">Canon-IPF6400</h2>
            <p class="text-sm text-gray-500">172.16.254.1</p>
          </div>
        </div>
        <div class="flex gap-4 ml-[-36px] ">
          <span class="flex items-center justify-center px-4 py-2  bg-cyan-500 rounded-full text-white">{{ jobCounts.inProgress }}</span>
          <span class="flex items-center justify-center px-4 py-2  bg-green-500 rounded-full text-white ">{{ jobCounts.pending }}</span>
          <span class="flex items-center justify-center px-4 py-2  bg-red-600 rounded-full text-white ">{{ jobCounts.error }}</span>
        </div>
      </div>
      <div class="flex flex-col w-1/2  mt-20 ml-24 mb-4">
        <div class="text-left text-black-800 font-semibold">Printing {{ progress }}%</div>
        <div class="bg-gray-200  w-[15vh] rounded-full h-2 dark:bg-gray-700 mt-2">
          <div class="bg-cyan-500 h-2 rounded-full" :style="{ width: progress + '%' }"></div>
        </div>
      </div>
    </div>
  </div>


</template>

<script>
export default {
  name: "PrinterStatus",
  data() {
    return {
      jobCounts: {
        inProgress: 147,
        pending: 89,
        error: 2,
      },
      progress: 64
    };
  }
};
</script>

<style>
@import "https://cdn.jsdelivr.net/npm/tailwindcss@latest/dist/tailwind.min.css";
.icon-background {
  background-color: #d2d2d2; 
  padding: 25px; 
  border-radius: 0.25rem; 
  display: inline-flex; 
  align-items: center;
  justify-content: center;
}
</style>
