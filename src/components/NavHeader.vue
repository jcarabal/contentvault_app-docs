<template>
  <header class="nav-header">
    <div class="header-container">
      <div class="logo-section">
        <div class="logo-icon">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <rect x="3" y="3" width="18" height="18" rx="2" stroke="currentColor" stroke-width="2"/>
            <path d="M12 8V16M8 12H16" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
          </svg>
        </div>
        <span class="logo-text">App Resources</span>
      </div>
      
      <nav class="nav-menu">
        <a href="#" class="nav-link active">Home</a>
        <a href="#apps" class="nav-link">Apps</a>
        <a href="#support" class="nav-link">Support</a>
        <a href="#contact" class="nav-link">Contact</a>
      </nav>
      
      <div class="search-section">
        <input 
          type="search" 
          placeholder="Search documentation..." 
          class="search-input"
        />
      </div>
    </div>
  </header>
</template>

<script setup lang="ts">
</script>

<style scoped>
.nav-header {
  background-color: #1a1a1a;
  border-bottom: 1px solid #333;
  padding: 1rem 0;
  position: sticky;
  top: 0;
  z-index: 100;
}

.header-container {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 2rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 2rem;
}

.logo-section {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.logo-icon {
  width: 32px;
  height: 32px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #5eead4;
}

.logo-text {
  font-size: 1.125rem;
  font-weight: 600;
  color: #fff;
}

.nav-menu {
  display: flex;
  gap: 2rem;
  flex: 1;
  justify-content: center;
}

.nav-link {
  color: #9ca3af;
  text-decoration: none;
  font-size: 0.9375rem;
  transition: color 0.2s;
  position: relative;
}

.nav-link:hover {
  color: #5eead4;
}

.nav-link.active {
  color: #5eead4;
}

.nav-link.active::after {
  content: '';
  position: absolute;
  bottom: -1.25rem;
  left: 0;
  right: 0;
  height: 2px;
  background-color: #5eead4;
}

.search-section {
  min-width: 250px;
}

.search-input {
  width: 100%;
  padding: 0.5rem 1rem;
  background-color: #0f0f0f;
  border: 1px solid #333;
  border-radius: 6px;
  color: #fff;
  font-size: 0.875rem;
  transition: border-color 0.2s;
}

.search-input::placeholder {
  color: #6b7280;
}

.search-input:focus {
  outline: none;
  border-color: #5eead4;
}

@media (max-width: 768px) {
  .header-container {
    flex-direction: column;
    gap: 1rem;
  }
  
  .nav-menu {
    width: 100%;
    justify-content: space-around;
  }
  
  .search-section {
    width: 100%;
  }
}
</style>
