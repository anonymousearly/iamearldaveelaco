<template>
  <v-footer
    app
    height="auto"
    class="d-flex justify-center align-center"
  >

    <strong>Follow me on</strong>
    <div class="d-flex ga-2 ms-auto">
    <v-btn v-for="icon in icons" :key="icon" :icon="icon" variant="plain" size="medium" />
  </div>
  </v-footer>
</template>

<script setup>
    const icons = [
    'mdi-github',
    'mdi-linkedin',
    'mdi-twitter',
    'mdi-instagram',
    'mdi-facebook',
    
  ]
</script>


