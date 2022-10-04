<template>
  <div>
    <div class="flex justify-center mt-8">
      <div class="w-[800px]">
        <div class="flex flex-row border-gray-300">
          <!-- Sidebar -->
          <div class="w-8 flex flex-col items-center gap-2 p-2 bg-gray-300 rounded-l-lg">
            <button 
              @click="marginOnRight = !marginOnRight"
              title="Click increase/decrease the width of the editor"
            >
              <IconChevronDoubleLeft v-if="!marginOnRight"/>
              <IconChevronDoubleRight v-else />
            </button>
            <button 
              @click="copyToClipBoard"
              title="Click to copy current text to the clipboard"
              class="active:animate-bounce transition duration-200 ease-in-out"
            >
              <IconClipboard />
            </button>
          </div>
          <!-- Text editor -->
          <div class="w-full" :class="marginOnRight ? 'mr-96' : ''">
            <textarea
              rows="30"
              name="plain_text"
              id="plain-text"
              v-model="plainText"
              :class="[
                'block w-full rounded-r-lg sm:text-sm font-mono',
                'focus:border-gray-300',
                'focus:ring-0',
                'border-gray-300',
                'border-l-0'
            ]"></textarea>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
  const marginOnRight = ref(false)
  const plainText = usePlainText()

  function copyToClipBoard() {
    navigator.clipboard.writeText(plainText.value)
  }
</script>