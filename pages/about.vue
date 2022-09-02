<template>
  <div>
    <div class="flex justify-center mt-4">
      <div class="w-[800px]">
        <p class="text-lg mx-auto max-w-md text-gray-500 text-center">
          A simple online no frills plain text editor.
        </p>
        <div class="bg-white m-4 border-gray-300 rounded-lg h-96">
          <div class="p-4 font-mono">
            <p class="pb-4">
              Plain Text Editor is a web-based plain text editor. It does not do
              anything fancy, but it useful for writing plain text.
            </p>
            <p class="pb-4">            
              I built Plain Text Editor because I was looking for a clean online
              text editor that would not mess up the formatting of plain text files
              such as markdown, but also plays nice with tools like <LinkExternal to="https://www.grammarly.com/">Grammarly</LinkExternal>.
            </p>
            <p class="pb-4">            
              The web-app is built using <LinkExternal to="https://vuejs.org">Vue 3</LinkExternal>
              / <LinkExternal to="https://v3.nuxtjs.org">Nuxt 3</LinkExternal>.
              You can find the source code at <LinkExternal to="https://github.com/SamEdwardes/plaintext-editor">github.com/SamEdwardes/plaintext-editor</LinkExternal>
            </p>
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
    navigator.clipboard.writeText(plainText.value)
  }
</script>