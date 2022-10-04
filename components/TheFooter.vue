<template>
  <footer class="bg-white">
    <div class="mx-auto max-w-7xl py-6 px-4 sm:px-6 lg:px-8">
      <div class=" md:flex md:items-center md:justify-between">
        <div class="mt-8  md:mt-0">
          <div class="flex flow-row justify-left gap-4 pb-2">
            <NuxtLink
              v-for="item in navLinks"
              :to="item.href"
              :key="item.text"
              class="text-base text-gray-400 hover:text-gray-500 underline underline-offset-4"
              :class="item.href === route.path ? ' decoration-indigo-500 decoration-4' : 'decoration-gray-500 decoration-2' "
            >
              {{ item.text }}
            </NuxtLink>
          </div>
          <p class="text-base text-gray-400">
            A simple plain text editor.
          </p>
          <p class="text-left text-base text-gray-400">&copy; Sam Edwardes</p>
        </div>
        <div class="mt-8  md:mt-0">
        </div>
        <div class="flex justify-center space-x-6">
          <a v-for="item in socialLinks" :key="item.name" :href="item.href" target="_blank" class="text-gray-400 hover:text-gray-500">
            <span class="sr-only">{{ item.name }}</span>
            <img :src="item.icon" class="h-6 w-6" aria-hidden="true"/>
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
const route = useRoute()

const socialLinks = ref([
  {
    name: 'GitHub',
    href: 'https://github.com/SamEdwardes/plaintext-editor',
    icon: '/imgs/GitHub-Mark-64px.png'
  }
])

const navLinks = ref([
  {
    href: '/',
    text: 'Home'
  },
  {
    href: '/about',
    text: 'About'
  },
])
</script>