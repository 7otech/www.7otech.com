<script setup>
import { ref } from 'vue'

const open = ref(false)

const links = [
  { name: '六大模块', href: '#modules' },
  { name: '工作流', href: '#workflow' },
  { name: '记忆与知识', href: '#memory' },
  { name: '安全治理', href: '#governance' },
]
</script>

<template>
  <header class="fixed top-0 inset-x-0 z-50 border-b border-white/5 bg-ink/80 backdrop-blur-md">
    <nav class="mx-auto flex max-w-7xl items-center justify-between px-6 py-4">
      <a href="#" class="flex items-center gap-2.5">
        <span class="flex h-8 w-8 items-center justify-center rounded-lg bg-gradient-to-br from-accent to-run text-sm font-bold text-white">B</span>
        <span class="text-lg font-semibold tracking-wide text-white">BioAgent <span class="text-accent-soft">OS</span></span>
      </a>

      <div class="hidden items-center gap-8 md:flex">
        <a
          v-for="link in links"
          :key="link.href"
          :href="link.href"
          class="text-sm text-gray-400 transition-colors hover:text-white"
        >{{ link.name }}</a>
        <a
          href="https://bioagent-new.7otech.com/"
          target="_blank"
          rel="noopener"
          class="rounded-lg bg-accent px-4 py-2 text-sm font-medium text-white transition-colors hover:bg-accent-soft"
        >进入门户</a>
      </div>

      <button class="md:hidden text-gray-300" @click="open = !open" aria-label="菜单">
        <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path v-if="!open" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
          <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
    </nav>

    <div v-if="open" class="border-t border-white/5 px-6 py-4 md:hidden">
      <a
        v-for="link in links"
        :key="link.href"
        :href="link.href"
        class="block py-2 text-sm text-gray-300"
        @click="open = false"
      >{{ link.name }}</a>
      <a
        href="https://bioagent-new.7otech.com/"
        target="_blank"
        rel="noopener"
        class="mt-2 block rounded-lg bg-accent px-4 py-2 text-center text-sm font-medium text-white"
      >进入门户</a>
    </div>
  </header>
</template>
