<template>
  <div>
    user-{{ route.params.group }}
  </div>
</template>
<script setup>
const route = useRoute()
</script>