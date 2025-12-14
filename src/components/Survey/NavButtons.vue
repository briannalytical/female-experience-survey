<template>
  <div class="flex items-center justify-between gap-4">
    <button
      :disabled="!canGoBack"
      @click="$emit('previous')"
      class="group relative px-6 py-3 bg-white rounded-xl shadow-md hover:shadow-lg transition-all duration-300 disabled:opacity-40 disabled:cursor-not-allowed flex items-center gap-2 border-2 border-slate-200 hover:border-blue-300"
    >
      <svg class="w-5 h-5 text-slate-600 group-hover:text-blue-600 transition-colors group-hover:-translate-x-1 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7" />
      </svg>
      <span class="font-semibold text-slate-700 group-hover:text-blue-600 transition-colors">
        Back
      </span>
    </button>

    <button
      :disabled="!canGoNext"
      @click="$emit('next')"
      class="group relative px-6 py-3 bg-gradient-to-r from-blue-500 to-blue-600 hover:from-blue-600 hover:to-blue-700 rounded-xl shadow-md hover:shadow-lg transition-all duration-300 disabled:opacity-40 flex items-center gap-2"
    >
      <span class="font-semibold text-white">Next</span>
      <svg class="w-5 h-5 text-white group-hover:translate-x-1 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
      </svg>
    </button>
  </div>
</template>

<script setup>
defineProps({
  canGoBack: Boolean,
  canGoNext: Boolean
})

defineEmits(['next', 'previous'])
</script>
