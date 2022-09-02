<template>
  <div>
    <div class="flex justify-center mt-8">
      <div class="w-[800px]">
        <div class="flex flex-row border-gray-300">
          <!-- Sidebar -->
          <div class="w-8 flex flex-col bg-gray-300 rounded-l-lg">
            <button @click="marginOnRight = !marginOnRight" class="m-1">
              <IconChevronDoubleLeft v-if="!marginOnRight"/>
              <IconChevronDoubleRight v-else />
            </button>
            <button @click="copyToClipBoard" class="m-1 pb-96">
              <IconClipboard />
            </button>
          </div>
          <!-- Text editor -->
          <div class="w-full" :class="marginOnRight ? 'mr-96' : ''">
            <textarea
              rows="30"
              name="plainText"
              id="plain-text"
              v-model="plainText"
              class="
                block w-full rounded-r-lg sm:text-sm font-mono
                 focus:border-gray-300
                focus:ring-0
                border-gray-300
                border-l-0
              "
            >
              {{ plainTextCookie }}
            </textarea>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
  const marginOnRight = ref(false)
  const plainText = ref('')

  function copyToClipBoard() {
    console.log(plainText.value)
    navigator.clipboard.writeText(plainText.value)
  }
</script>