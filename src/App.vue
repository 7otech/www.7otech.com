<script setup>
import NavBar from './components/NavBar.vue'
import HeroSection from './components/HeroSection.vue'
import ModulesSection from './components/ModulesSection.vue'
import WorkflowSection from './components/WorkflowSection.vue'
import MemorySection from './components/MemorySection.vue'
import GovernanceSection from './components/GovernanceSection.vue'
import CtaSection from './components/CtaSection.vue'
import FooterSection from './components/FooterSection.vue'
</script>

<template>
  <div class="min-h-screen bg-ink">
    <NavBar />
    <main>
      <HeroSection />
      <ModulesSection />
      <WorkflowSection />
      <MemorySection />
      <GovernanceSection />
      <CtaSection />
    </main>
    <FooterSection />
  </div>
</template>
