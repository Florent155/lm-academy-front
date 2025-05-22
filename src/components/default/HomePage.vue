<script setup>
import { onMounted, ref } from 'vue'

const quote = ref('')
const author = ref('')
const quoteLines = ref([]) 

const fetchZenQuotesApi = async () => {
  try {
    const response = await fetch('http://localhost:8000/api/zen-quote')
    const data = await response.json()
    console.log("data", data)
    if (data.success) {
      quote.value = data.quote.text
      author.value = data.quote.author
    } else {
      quote.value = "The world would go on even without you. Don't take yourself so seriously."
      author.value = "Norman Vincent Peale"
    }

    quoteLines.value = quote.value.split(/(?<=[.!?])\s+/).slice(0, 3)
  } catch (error) {
    console.error('Error fetching quote:', error)
  }
}

onMounted(() => {
  fetchZenQuotesApi()
})
</script>

<template>
  <div class="relative min-h-screen bg-[#F2F7FC] flex flex-col">
  
    <div class="flex-grow pt-24 flex items-start justify-center">
      <div class="text-center">
        <h1 class="text-4xl font-medium leading-relaxed">
          Welcome to LM Academy<br />
          Empowering Students with the<br />
          Skills of Tomorrow
        </h1>
      </div>
    </div>

<div class="absolute right-10 bottom-[18%] text-end leading-tight">
  <p class="italic text-[#003366] font-gelasio text-[26px] leading-snug text-right">
    <span class="block pl-0">{{ quoteLines[0] || 'Loading...' }}</span>
    <span class="block pl-4" v-if="quoteLines[1]">{{ quoteLines[1] }}</span>
    <span class="block pl-8" v-if="quoteLines[2]">{{ quoteLines[2] }}</span>
  </p>
  <p class="text-[#8694A9] text-sm mt-1">— {{ author || "Unknown" }}</p>
</div>
  </div>
</template>
