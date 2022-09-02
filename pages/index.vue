<template>
  <div class="flex justify-center">
    <div class="w-[800px]">
      <ButtonBase @click="marginOnRight = !marginOnRight" class="basis-1/6 text-right">Space on Right</ButtonBase>
      <div class="mt-1" :class="marginOnRight ? 'mr-96' : ''">
        <textarea 
          rows="30" 
          name="comment" 
          id="comment" 
          :class="[
            'block w-full rounded-md border-gray-300 shadow-lg',
            'focus:border-indigo-500 focus:ring-indigo-500',
            'sm:text-sm font-mono'
          ]" 
        />
      </div>
    </div>
  </div>
</template>

<script setup>
  const marginOnRight = ref(false)
</script>