<script setup>
const stats = [
  { value: '6', label: '核心功能模块' },
  { value: '3 档', label: '模型信任级别' },
  { value: '100%', label: '审计留痕覆盖' },
  { value: '内网', label: '样本数据红线' },
]
</script>

<template>
  <section class="relative overflow-hidden pt-36 pb-24">
    <!-- 背景光晕 -->
    <div class="pointer-events-none absolute inset-0">
      <div class="absolute -top-40 left-1/2 h-[480px] w-[720px] -translate-x-1/2 rounded-full bg-accent/15 blur-[120px]"></div>
      <div class="absolute top-40 right-0 h-72 w-72 rounded-full bg-run/10 blur-[100px]"></div>
    </div>

    <div class="relative mx-auto max-w-7xl px-6 text-center">
      <div class="mx-auto mb-6 inline-flex items-center gap-2 rounded-full border border-accent/30 bg-accent/10 px-4 py-1.5 text-xs text-accent-soft">
        <span class="h-1.5 w-1.5 animate-pulse rounded-full bg-accent"></span>
        面向生命科学研究的 AI Agent 平台
      </div>

      <h1 class="mx-auto max-w-4xl text-4xl font-bold leading-tight text-white sm:text-6xl sm:leading-[1.15]">
        让每一次生信分析<br />
        <span class="bg-gradient-to-r from-accent-soft via-accent to-run bg-clip-text text-transparent">可复现 · 可审计 · 可进化</span>
      </h1>

      <p class="mx-auto mt-6 max-w-2xl text-base leading-relaxed text-gray-400 sm:text-lg">
        BioAgent OS 将项目、会话、画布、报告、数据、技能组织为一个统一的研究操作系统。
        AI 智能体在受控的执行环境中编排分析流水线，沉淀长期记忆与领域知识，让科研团队专注问题本身。
      </p>

      <div class="mt-10 flex flex-col items-center justify-center gap-4 sm:flex-row">
        <a
          href="https://bioagent-new.7otech.com/"
          target="_blank"
          rel="noopener"
          class="w-full rounded-xl bg-accent px-8 py-3.5 text-sm font-semibold text-white shadow-lg shadow-accent/25 transition-all hover:bg-accent-soft hover:shadow-accent/40 sm:w-auto"
        >立即进入门户 →</a>
        <a
          href="#modules"
          class="w-full rounded-xl border border-white/10 bg-white/5 px-8 py-3.5 text-sm font-semibold text-gray-200 transition-colors hover:bg-white/10 sm:w-auto"
        >了解六大模块</a>
      </div>

      <dl class="mx-auto mt-20 grid max-w-3xl grid-cols-2 gap-6 sm:grid-cols-4">
        <div v-for="s in stats" :key="s.label" class="rounded-2xl border border-white/5 bg-ink-soft/60 px-4 py-6">
          <dt class="text-2xl font-bold text-white sm:text-3xl">{{ s.value }}</dt>
          <dd class="mt-1 text-xs text-gray-500">{{ s.label }}</dd>
        </div>
      </dl>
    </div>
  </section>
</template>
