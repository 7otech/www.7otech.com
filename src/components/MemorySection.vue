<script setup>
const features = [
  {
    title: '跨会话记忆',
    desc: '长期记忆以 Markdown 记录，开启后自动注入最近相关条目，让智能体记得项目的来龙去脉。',
  },
  {
    title: '执行记忆',
    desc: '每次运行的经验自动沉淀归档，越用越懂你的分析习惯与数据特点。',
  },
  {
    title: '知识库',
    desc: '文献、方法卡与领域插件构成领域知识底座，为智能体决策提供专业依据。',
  },
  {
    title: '上下文压缩',
    desc: '会话级上下文压缩自动执行，长项目对话不丢失关键信息。',
  },
]
</script>

<template>
  <section id="memory" class="relative py-24">
    <div class="pointer-events-none absolute inset-0">
      <div class="absolute bottom-0 left-0 h-72 w-72 rounded-full bg-accent/10 blur-[100px]"></div>
    </div>

    <div class="relative mx-auto max-w-7xl px-6">
      <div class="grid items-center gap-14 lg:grid-cols-2">
        <div>
          <p class="text-sm font-medium tracking-widest text-accent-soft">SELF-EVOLVING MEMORY</p>
          <h2 class="mt-3 text-3xl font-bold text-white sm:text-4xl">自进化记忆<br />让平台随研究一起成长</h2>
          <p class="mt-5 leading-relaxed text-gray-400">
            传统生信工具用完即走，知识散落在笔记与聊天记录里。BioAgent OS 把记忆作为一等公民：
            人写的长期记忆、机器沉淀的执行记忆、领域知识库三者协同，构成平台的自进化记忆体系。
          </p>
          <div class="mt-8 grid gap-4 sm:grid-cols-2">
            <div
              v-for="f in features"
              :key="f.title"
              class="rounded-xl border border-white/5 bg-ink-soft/60 p-5"
            >
              <h3 class="text-sm font-semibold text-white">{{ f.title }}</h3>
              <p class="mt-2 text-xs leading-relaxed text-gray-400">{{ f.desc }}</p>
            </div>
          </div>
        </div>

        <!-- 示意：记忆编辑器 -->
        <div class="rounded-2xl border border-white/10 bg-ink-soft/80 p-1 shadow-2xl shadow-accent/5">
          <div class="rounded-xl bg-ink/90 p-6">
            <div class="flex items-center justify-between border-b border-white/5 pb-4">
              <div class="flex items-center gap-2">
                <span class="h-2.5 w-2.5 rounded-full bg-red-500/70"></span>
                <span class="h-2.5 w-2.5 rounded-full bg-yellow-500/70"></span>
                <span class="h-2.5 w-2.5 rounded-full bg-done/70"></span>
              </div>
              <span class="text-xs text-gray-500">长期记忆 · RNA-seq 差异分析约定</span>
            </div>
            <div class="mt-5 space-y-3 font-mono text-xs leading-relaxed">
              <p class="text-accent-soft"># 差异表达分析约定</p>
              <p class="text-gray-400">- 计数矩阵需 <span class="text-white">abundance</span> 字段</p>
              <p class="text-gray-400">- 默认使用 DESeq2，阈值 padj &lt; 0.05</p>
              <p class="text-gray-400">- 样本数据 <span class="text-done">仅限内网</span>，禁止出域</p>
              <p class="mt-4 text-accent-soft">## 执行记忆 · 自动归档</p>
              <p class="text-gray-500">2026-09-05 运行 #128 · 火山图产物已归集到报告</p>
              <p class="text-gray-500">2026-09-06 运行 #131 · 队列等待 2min · 预热镜像命中</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
