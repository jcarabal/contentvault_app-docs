<template>
  <footer class="footer-section">
    <div class="footer-container">
      <div class="footer-left">
        <p class="copyright">© 2025 App Resources. All rights reserved.</p>
      </div>
      <div class="footer-center">
        <a href="#support" class="footer-link">Support & Help</a>
        <span class="separator">•</span>
        <a href="#github" class="footer-link">GitHub</a>
      </div>
      <div class="footer-right">
        <p class="last-updated">Last Updated: November 17, 2025</p>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
</script>

<style scoped>
.footer-section {
  background-color: #0f0f0f;
  border-top: 1px solid #333;
  padding: 2rem 0;
  margin-top: auto;
}

.footer-container {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 2rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 2rem;
  flex-wrap: wrap;
}

.footer-left,
.footer-right {
  flex: 1;
}

.footer-center {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.copyright,
.last-updated {
  color: #6b7280;
  font-size: 0.875rem;
  margin: 0;
}

.footer-right {
  text-align: right;
}

.footer-link {
  color: #9ca3af;
  text-decoration: none;
  font-size: 0.875rem;
  transition: color 0.2s;
}

.footer-link:hover {
  color: #5eead4;
}

.separator {
  color: #4b5563;
}

@media (max-width: 768px) {
  .footer-container {
    flex-direction: column;
    text-align: center;
  }
  
  .footer-right {
    text-align: center;
  }
}
</style>
