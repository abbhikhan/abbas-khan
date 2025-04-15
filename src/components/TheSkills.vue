<template>
    <v-container class="skills-container">
      <v-row>
        <v-col cols="12" class="text-center mb-2">
          <h2 class="text-h3 font-weight-bold">My Skills</h2>
          <p class="text-subtitle-1 text-grey-darken-1">Technologies I've mastered</p>
        </v-col>
      </v-row>
  
      <!-- Core Development -->
      <v-row class="mb-6">
        <v-col cols="12">
          <h3 class="text-h5 font-weight-bold mb-4">Core Development</h3>
          <div class="d-flex flex-wrap ga-3">
            <v-chip variant="flat" color="deep-purple" size="large" prepend-icon="mdi-code-tags">
              Dart
            </v-chip>
            <v-chip variant="flat" color="blue" size="large" prepend-icon="mdi-cellphone">
              Flutter
            </v-chip>
          </div>
        </v-col>
      </v-row>
  
      <!-- UI/UX -->
      <v-row class="mb-6">
        <v-col cols="12">
          <h3 class="text-h5 font-weight-bold mb-4">UI/UX Expertise</h3>
          <div class="d-flex flex-wrap ga-3">
            <v-chip variant="flat" color="indigo" size="large" prepend-icon="mdi-palette">
              UI Expert
            </v-chip>
            <v-chip variant="flat" color="pink" size="large" prepend-icon="mdi-animation">
              Animations
            </v-chip>
            <v-chip variant="flat" color="teal" size="large" prepend-icon="mdi-responsive">
              Responsiveness
            </v-chip>
          </div>
        </v-col>
      </v-row>
  
      <!-- Platform Development -->
      <v-row class="mb-6">
        <v-col cols="12">
          <h3 class="text-h5 font-weight-bold mb-4">Platform Development</h3>
          <div class="d-flex flex-wrap ga-3">
            <v-chip variant="flat" color="black" size="large" prepend-icon="mdi-apple">
              iOS App Development
            </v-chip>
            <v-chip variant="flat" color="orange" size="large" prepend-icon="mdi-android">
              Android App Development
            </v-chip>
            <v-chip variant="flat" color="green" size="large" prepend-icon="mdi-google-play">
              PlayStore Management
            </v-chip>
            <v-chip variant="flat" color="blue-grey" size="large" prepend-icon="mdi-apple">
              App Store Management
            </v-chip>
          </div>
        </v-col>
      </v-row>
  
      <!-- Backend & APIs -->
      <v-row class="mb-6">
        <v-col cols="12">
          <h3 class="text-h5 font-weight-bold mb-4">Backend & APIs</h3>
          <div class="d-flex flex-wrap ga-3">
            <v-chip variant="flat" color="orange" size="large" prepend-icon="mdi-api">
              API Integration
            </v-chip>
            <v-chip variant="flat" color="amber" size="large" prepend-icon="mdi-firebase">
              Firebase Storage
            </v-chip>
            <v-chip variant="flat" color="deep-orange" size="large" prepend-icon="mdi-firebase">
              Firebase Messaging
            </v-chip>
            <v-chip variant="flat" color="red" size="large" prepend-icon="mdi-bell">
              Firebase Notifications
            </v-chip>
          </div>
        </v-col>
      </v-row>
  
      <!-- Services & Integrations -->
      <v-row class="mb-6">
        <v-col cols="12">
          <h3 class="text-h5 font-weight-bold mb-4">Services & Integrations</h3>
          <div class="d-flex flex-wrap ga-3">
            <v-chip variant="flat" color="blue-darken-2" size="large" prepend-icon="mdi-google-maps">
              Google Maps
            </v-chip>
            <v-chip variant="flat" color="green-darken-2" size="large" prepend-icon="mdi-credit-card">
              Payment Gateways
            </v-chip>
            <v-chip variant="flat" color="red-darken-2" size="large" prepend-icon="mdi-advertisements">
              Google Ads
            </v-chip>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script setup>
  // No script needed for basic implementation
  </script>
  
  <style scoped>
  .skills-container {
    max-width: 1200px;
    padding-top: 64px;
    padding-bottom: 64px;
  }
  
  .v-chip {
    transition: transform 0.2s;
  }
  
  .v-chip:hover {
    transform: translateY(-3px);
  }
  </style>