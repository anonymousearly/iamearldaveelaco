<template>
    <v-container class="pa-4">
      <v-card class="pa-6 rounded-lg" elevation="3">
        <v-row align="center">
          <!-- Left Side (Text Content) -->
          <v-col cols="12" md="8">
            <h1 class="text-h4 font-weight-bold">
              Hello! I am Earl Dave
            </h1>
            <p class="text-subtitle-1">
              I am a 22 year-old Mobile and Web Developer from the Philippines 🇵🇭
            </p>
  
            <p class="font-weight-medium mt-6">
              For any Q&A, raise a ticket with Earl Support
              <v-icon>mdi-arrow-right</v-icon>
            </p>
  
            <v-btn class="mt-4 mr-4" variant="outlined" prepend-icon="mdi-download">
              Resume
            </v-btn>
  
            <!-- Social Icons -->
            <div class="mt-4">
              <v-btn
                v-for="icon in icons"
                :key="icon.name"
                :icon="icon.name"
                :href="icon.link"
                target="_blank"
                class="mr-2"
                variant="plain"
              >
                <v-icon>{{ icon.name }}</v-icon>
              </v-btn>
            </div>
          </v-col>
  
          <!-- Right Side (Image with Dialog) -->
          <v-col cols="12" md="4" class="text-center">
            <v-dialog max-width="600">
              <template v-slot:activator="{ props: activatorProps }">
                <v-img
                  src="@/assets/earldave.png"
                  alt="Earl Dave"
                  max-width="200"
                  class="rounded-lg mx-auto cursor-pointer"
                  v-bind="activatorProps"
                ></v-img>
              </template>
  
              <template v-slot:default="{ isActive }">
                <v-card class="rounded-lg overflow-hidden">
                  <v-img
                    src="@/assets/earldave.png"
                    alt="Zoomed Earl Dave"
                    aspect-ratio="1"
                    cover
                  ></v-img>
                  <v-card-actions>
                    <v-spacer></v-spacer>
                    <v-btn text="Close" @click="isActive.value = false"></v-btn>
                  </v-card-actions>
                </v-card>
              </template>
            </v-dialog>
          </v-col>
        </v-row>
      </v-card>
    </v-container>
  </template>
  
  <script setup>
  const icons = [
    { name: 'mdi-linkedin', link: 'https://www.linkedin.com/in/chuykooshot/' },
    { name: 'mdi-github', link: 'https://github.com/anonymousearly' },
    { name: 'mdi-email', link: 'mailto:elaco.earl13@gmail.com' },
  ]
  </script>