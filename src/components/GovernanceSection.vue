<script setup>
const items = [
  {
    icon: '🔒',
    title: '样本数据红线',
    desc: '受控样本严禁出内网，数据导出默认禁止、需走审批流程，对象存储 MinIO 统一管控。',
  },
  {
    icon: '🎚️',
    title: '三档信任级别',
    desc: '模型信任档位三档全局生效，涉及执行的操作需方案确认后才放行，AI 不越权。',
  },
  {
    icon: '📜',
    title: '审计全留痕',
    desc: '五角色权限体系，审计日志覆盖参数、版本与产物，每一次操作都可追溯。',
  },
  {
    icon: '🐳',
    title: '受控执行环境',
    desc: '容器运行时 + Docker 降级链 + 预热镜像 + 任务队列，RuntimeDetector 实时监控执行环境健康。',
  },
]
</script>

<template>
  <section id="governance" class="relative border-y border-white/5 bg-ink-soft/40 py-24">
    <div class="mx-auto max-w-7xl px-6">
      <div class="text-center">
        <p class="text-sm font-medium tracking-widest text-accent-soft">GOVERNANCE & SECURITY</p>
        <h2 class="mt-3 text-3xl font-bold text-white sm:text-4xl">为科研数据而生的安全治理</h2>
        <p class="mx-auto mt-4 max-w-2xl text-gray-400">
          AI 能力越强，边界越要清晰。BioAgent OS 在系统层内置治理，而不是事后补丁。
        </p>
      </div>

      <div class="mt-16 grid gap-6 sm:grid-cols-2 lg:grid-cols-4">
        <div
          v-for="item in items"
          :key="item.title"
          class="rounded-2xl border border-white/5 bg-ink/60 p-7 transition-colors hover:border-accent/30"
        >
          <span class="text-3xl">{{ item.icon }}</span>
          <h3 class="mt-4 text-base font-semibold text-white">{{ item.title }}</h3>
          <p class="mt-3 text-sm leading-relaxed text-gray-400">{{ item.desc }}</p>
        </div>
      </div>
    </div>
  </section>
</template>
