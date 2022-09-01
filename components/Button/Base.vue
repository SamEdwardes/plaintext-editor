<template>
  <button 
    type="button" 
    :class="['flex w-full items-center justify-center rounded-md border',
      'border-transparent bg-indigo-500 py-2 px-4', 
      'text-base font-medium text-white hover:bg-indigo-600',
      'focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2', 
      'focus:ring-offset-gray-800'
    ]"
  >
    <slot />
  </button>
</template>