<template>
    <v-tabs v-model="tab" align-tabs="center">    
        <v-tab value="home">
            <v-icon>mdi-home</v-icon>
            Home
        </v-tab>
        <v-tab value="projects">
            <v-icon>mdi-star-box-multiple-outline</v-icon>
            Projects
        </v-tab>
        <v-tab value="contact">
            <v-icon>mdi-contacts-outline</v-icon>
            Contact Me
        </v-tab>
        <v-btn :icon="themeIcon" @click="toggleTheme" variant="plain">
            
        </v-btn>
    </v-tabs>
    
</template>

<script setup>
import { ref, computed } from 'vue';
import { useTheme } from 'vuetify'

const theme = useTheme()
const tab = ref('home');

const toggleTheme = () => {
  theme.global.name.value = theme.global.name.value === 'dark' ? 'light' : 'dark'
};

const themeIcon = computed(() =>
    theme.global.name.value === 'dark' ? 'mdi-weather-night' : 'mdi-white-balance-sunny'
);

</script>
