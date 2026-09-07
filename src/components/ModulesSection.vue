<script setup>
const modules = [
  {
    icon: '🧬',
    name: '项目',
    en: 'Project',
    desc: '一切研究以项目为中心组织。数据集、会话、流水线、记忆与报告全部归集到项目之下，置顶、重命名、切换一目了然。',
    points: ['项目级数据与会话归集', '跨项目快速切换', '新建 · 置顶 · 归档管理'],
  },
  {
    icon: '💬',
    name: '会话',
    en: 'Session',
    desc: '普通会话用于对话协商，项目会话沉淀项目内所有讨论。快速提问跨屏唤起，上下文自动携带，不打断当前工作。',
    points: ['普通会话 / 项目会话双轨', '跨屏快速提问 · 上下文自动携带', '会话暂停 / 继续 / 归档'],
  },
  {
    icon: '🕸️',
    name: '画布',
    en: 'Canvas',
    desc: '可视化编排分析流水线。节点语义契约自动匹配数据集槽位，锁定并执行一次分析，流水线可保存、复用与置顶。',
    points: ['节点式流水线编排', '语义过滤 · 数据集槽位自动拆出', '锁定执行 · 流水线复用'],
  },
  {
    icon: '📊',
    name: '报告',
    en: 'Report',
    desc: '每次运行的产物与参数自动汇聚为结构化报告，实验级成本归集到可复现坐标，一键导出分享。',
    points: ['运行产物自动汇聚', '成本 · 参数 · 版本全留痕', '报告导出与复现坐标'],
  },
  {
    icon: '🗄️',
    name: '数据',
    en: 'Data',
    desc: '项目数据集、公共数据集、本地样本库与参考库统一管理，对象存储 MinIO 支撑，受控样本仅限内网。',
    points: ['项目 / 公共 / 本地样本库', '文件上传与数据集绑定', '受控样本内网红线'],
  },
  {
    icon: '🧩',
    name: '技能',
    en: 'Skill',
    desc: '注册与管理领域分析技能，AI 智能体按任务自动调度，方法卡与领域插件持续扩展平台能力边界。',
    points: ['技能注册与语义检索', '智能体自动调度', '领域插件持续扩展'],
  },
]
</script>

<template>
  <section id="modules" class="relative py-24">
    <div class="mx-auto max-w-7xl px-6">
      <div class="text-center">
        <p class="text-sm font-medium tracking-widest text-accent-soft">SIX MODULES</p>
        <h2 class="mt-3 text-3xl font-bold text-white sm:text-4xl">六大模块，一个研究操作系统</h2>
        <p class="mx-auto mt-4 max-w-2xl text-gray-400">
          从提出问题到产出报告，BioAgent OS 覆盖了生信研究的完整闭环。
        </p>
      </div>

      <div class="mt-16 grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
        <div
          v-for="m in modules"
          :key="m.name"
          class="group rounded-2xl border border-white/5 bg-ink-soft/60 p-7 transition-all hover:border-accent/40 hover:bg-ink-soft"
        >
          <div class="flex items-center gap-3">
            <span class="text-2xl">{{ m.icon }}</span>
            <div>
              <h3 class="text-lg font-semibold text-white">{{ m.name }}</h3>
              <p class="text-xs tracking-wider text-gray-500 uppercase">{{ m.en }}</p>
            </div>
          </div>
          <p class="mt-4 text-sm leading-relaxed text-gray-400">{{ m.desc }}</p>
          <ul class="mt-5 space-y-2">
            <li v-for="p in m.points" :key="p" class="flex items-start gap-2 text-xs text-gray-400">
              <span class="mt-1 h-1 w-1 shrink-0 rounded-full bg-accent"></span>{{ p }}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>
