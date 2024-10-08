<template>
  <div id="services" class="cards">
    <CardProject />
  </div>
</template>

<script>
import CardProject from '@/components/CardProject.vue'

export default {
  name: 'ServicesPage',
  components: {
    CardProject
  }
}
</script>

<style scoped>
.cards {
  min-height: 100vh;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
