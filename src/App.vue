<script setup>
import HomePage from '@/views/HomePage.vue'
import ServicesPage from './views/ServicesPage.vue'
import AboutPage from './views/AboutPage.vue'
import PortfolioPage from './views/PortfolioPage.vue'
import ContactPage from './views/ContactPage.vue'
import FooterPage from './components/FooterPage.vue'
</script>

<template>
  <header></header>

  <main>
    <HomePage />
    <ServicesPage />
    <AboutPage />
    <PortfolioPage />
    <ContactPage />
    <FooterPage />
  </main>
</template>

<style scoped></style>
