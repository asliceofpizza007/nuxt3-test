<template>
  <p>
    {{ group }} - {{ id }}
  </p>
</template>
<script setup>
const route = useRoute()
const {
  group,
  id,
} = route.params

definePageMeta({
  title: 'My home page'
})

</script>