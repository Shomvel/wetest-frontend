<template>users {{ route.params.id }}</template>

<script setup lang="ts">
const route = useRoute()
const count = ref(1)
</script>