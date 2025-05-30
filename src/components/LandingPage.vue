<template>
    
    <v-container fluid justify="center" fill-height class="pa-6">
        
        <v-row justify="center" align-md="center">

            <!--- Left side of the row, specifically for my important information --->
            <v-col cols="12" md="4" class="center">
            <h1 class="text-h3 font-weight-bold mb-6 ">
            Earl Dave Elaco
        </h1>
        <p class="text-h5 font-weight-bold opacity-80">
            Junior Frontend Developer
        </p>
        <p class="text-h5 font-weight-bold opacity-80">
            Based from the Philippines 🇵🇭
            <v-icon icon="mdi-map-maker"></v-icon>
        </p>

        <div class="mt-2">
            <v-btn
                v-for="icon in icons"
                :key="icon.name"
                :icon="icon.name"
                :href="icon.link"
                target="_blank"
                variant="plain"
              ></v-btn>
              <v-btn 
                rounded 
                prepend-icon="mdi-download">
              Resume
            </v-btn>
        </div>

            </v-col>

        <!-- Right Side (Image with Dialog) -->
        <v-col cols="12" md="3">
            <v-dialog max-width="600">
              <template v-slot:activator="{ props: activatorProps }">
                <v-img
                  src="@/assets/earldave.png"
                  alt="Earl Dave"
                  max-width="100%"
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
        
        
    </v-container>


</template>


<script setup>
  const icons = [
    { name: 'mdi-linkedin', link: 'https://www.linkedin.com/in/chuykooshot/' },
    { name: 'mdi-github', link: 'https://github.com/anonymousearly' },
    { name: 'mdi-facebook', link: 'https://www.facebook.com/chuykooshot'},
  ]
</script>