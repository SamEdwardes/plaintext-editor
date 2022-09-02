<template>
  <span class="inline">
    <NuxtLink
      :to="to"
      target="_blank"
      class="text-indigo-500 hover:text-indigo-700 hover:underline underline-offset-4 decoration-indigo-700"
    >
        <slot />
        <IconArrowTopRightOnSquare class="inline" />
    </NuxtLink>
  </span>
</template>

<script setup>
  defineProps({
    to: {
      type: String,
      default: "#"
    }
  })
</script>