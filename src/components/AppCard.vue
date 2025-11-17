<template>
  <div class="app-card" :class="{ 'is-beta': isBeta }">
    <div class="card-icon">
      <svg width="32" height="32" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <rect x="3" y="3" width="18" height="18" rx="2" stroke="currentColor" stroke-width="2"/>
        <path d="M9 9H15M9 13H12" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
      </svg>
    </div>
    
    <h3 class="app-title">{{ title }}</h3>
    <p class="app-description">{{ description }}</p>
    
    <div class="card-links">
      <a v-for="link in links" :key="link" href="#" class="doc-link">{{ link }}</a>
    </div>
  </div>
</template>

<script setup lang="ts">
interface Props {
  title: string
  description: string
  links: string[]
  isBeta?: boolean
}

defineProps<Props>()
</script>

<style scoped>
.app-card {
  background-color: #1f1f1f;
  border: 1px solid #333;
  border-radius: 12px;
  padding: 2rem;
  transition: all 0.3s;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.app-card:hover {
  border-color: #5eead4;
  transform: translateY(-4px);
  box-shadow: 0 10px 30px rgba(94, 234, 212, 0.1);
}

.app-card.is-beta {
  background: linear-gradient(135deg, rgba(94, 234, 212, 0.1) 0%, rgba(20, 184, 166, 0.05) 100%);
  border-color: #5eead4;
}

.card-icon {
  width: 48px;
  height: 48px;
  background-color: #0f0f0f;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #5eead4;
}

.app-title {
  font-size: 1.25rem;
  font-weight: 600;
  color: #fff;
  margin: 0;
}

.app-description {
  color: #9ca3af;
  font-size: 0.875rem;
  margin: 0;
  line-height: 1.6;
}

.card-links {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  margin-top: 0.5rem;
}

.doc-link {
  color: #d1d5db;
  text-decoration: none;
  font-size: 0.875rem;
  transition: color 0.2s;
  padding: 0.25rem 0;
}

.doc-link:hover {
  color: #5eead4;
}
</style>
