<template>
  <p className="message">{{message}}</p>
</template>

<script setup>
const props = defineProps({
     message:String,
})
</script>

<style>

</style>