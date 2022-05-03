<template>
  <NuxtPage />
  <div>
    {{ counter }}
  </div>
  <div>
    Counter: {{ counter }}
    <button @click="counter++">
      ++
    </button>
    <button @click="counter--">
      --
    </button>
  </div>
  <div v-if="pending">
    pending
  </div>
  <div v-else>
    <span>{{ mt.blog }}</span>
    <span>{{ mt.location }}</span>
  </div> 
  <button @click="refresh">
    click
  </button>
</template>
<script setup>
const counter = useCookie('counter')
counter.value = 50

const { data: mt, pending, error, refresh } = await useFetch(
  'https://api.github.com/orgs/nuxt',
  {
    pick: [
      'blog',
      'location',
    ]
  }
)


</script>