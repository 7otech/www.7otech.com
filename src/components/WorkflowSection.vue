<script setup>
const steps = [
  {
    no: '01',
    title: '创建项目，绑定数据',
    desc: '新建项目并上传或选取数据集，画布节点的输入契约会对数据集做语义过滤，只显示匹配的候选，选完即走、回到画布。',
    color: 'text-accent-soft',
    ring: 'border-accent/30 bg-accent/10',
  },
  {
    no: '02',
    title: '画布编排流水线',
    desc: '在画布上拖拽节点编排分析流程，技能与模型由智能体自动调度，确认方案后锁定并执行一次分析。',
    color: 'text-run',
    ring: 'border-run/30 bg-run/10',
  },
  {
    no: '03',
    title: '运行受控执行',
    desc: '任务进入队列，在容器化执行环境中运行（Docker 降级链 + 预热镜像），执行通知覆盖完成、失败与需确认三种状态。',
    color: 'text-run',
    ring: 'border-run/30 bg-run/10',
  },
  {
    no: '04',
    title: '报告沉淀与复现',
    desc: '参数、版本与产物全量留痕，实验级成本归集到报告的可复现坐标，执行记忆自动归档，喂养下一次分析。',
    color: 'text-done',
    ring: 'border-done/30 bg-done/10',
  },
]
</script>

<template>
  <section id="workflow" class="relative border-y border-white/5 bg-ink-soft/40 py-24">
    <div class="mx-auto max-w-7xl px-6">
      <div class="text-center">
        <p class="text-sm font-medium tracking-widest text-accent-soft">WORKFLOW</p>
        <h2 class="mt-3 text-3xl font-bold text-white sm:text-4xl">从问题到报告，四步闭环</h2>
      </div>

      <div class="mt-16 grid gap-6 md:grid-cols-2 lg:grid-cols-4">
        <div
          v-for="(s, i) in steps"
          :key="s.no"
          class="relative rounded-2xl border border-white/5 bg-ink/60 p-7"
        >
          <span :class="['inline-flex h-10 w-10 items-center justify-center rounded-xl border text-sm font-bold', s.ring, s.color]">
            {{ s.no }}
          </span>
          <h3 class="mt-5 text-base font-semibold text-white">{{ s.title }}</h3>
          <p class="mt-3 text-sm leading-relaxed text-gray-400">{{ s.desc }}</p>
          <span
            v-if="i < steps.length - 1"
            class="absolute top-1/2 -right-3 hidden -translate-y-1/2 text-gray-600 lg:block"
          >→</span>
        </div>
      </div>
    </div>
  </section>
</template>
