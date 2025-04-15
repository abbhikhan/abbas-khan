<template>
  <v-container class="projects-container">
    <!-- Header Section -->
    <v-row class="mb-8">
      <v-col cols="12" class="text-center">
        <h1 class="text-h3 font-weight-bold mb-2">My Projects</h1>
        <p class="text-subtitle-1 text-grey-darken-1">
          A collection of my recent work and contributions
        </p>
      </v-col>
    </v-row>

    <!-- Projects Grid -->
    <v-row>
      <v-col
        v-for="(project, index) in projects"
        :key="index"
        cols="12"
        sm="6"
        md="4"
        lg="4"
      >
        <v-card
          class="project-card mx-auto"
          elevation="4"
          max-width="400"
          @click="openProject(project)"
        >
          <!-- Project Image -->
          <v-img
            :src="project.image"
            height="200"
            cover
            class="align-end"
            gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
          >
            <v-card-title class="text-white">{{ project.title }}</v-card-title>
          </v-img>

          <!-- Project Details -->
          <v-card-text>
            <div class="d-flex flex-wrap ga-2 mb-3">
              <v-chip
                v-for="(tech, i) in project.technologies"
                :key="i"
                size="small"
                variant="outlined"
                color="primary"
              >
                {{ tech }}
              </v-chip>
            </div>
            <p class="text-body-1">{{ project.description }}</p>
          </v-card-text>

          <!-- Action Buttons -->
          <v-card-actions>
            <v-btn
              variant="text"
              color="primary"
              :href="project.demoUrl"
              target="_blank"
              prepend-icon="mdi-web"
            >
              Live Demo
            </v-btn>
            <!-- <v-btn
              variant="text"
              color="secondary"
              :href="project.codeUrl"
              target="_blank"
              prepend-icon="mdi-github"
            >
              View Code
            </v-btn> -->
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
import { ref } from "vue";

const projects = ref([
  {
    title: "NeoHealth Home Healthcare",
    description:
      "NeoHealth is your go-to app for booking doctor appointments seamlessly. With a wide range of healthcare professionals, find and schedule consultations in just a few taps. Stay healthy, stay connected with the best doctors at your convenience.",
    technologies: ["Flutter", "Firebase", "Dart", "Google Pay","Fast Api"],
    image: require("@/assets/neohealth.jpeg"),
    demoUrl: "https://play.google.com/store/apps/details?id=ae.neohealth.app",
    codeUrl: "#",
  },
  {
    title: "Sea Dubai",
    description:
      "SeaDubai is your ultimate guide to exploring the best tourist spots in Dubai. Discover hidden gems, iconic landmarks, and exciting activities with easy-to-use maps and recommendations. Make the most of your Dubai adventure with personalized itineraries and insider tips.",
    technologies: ["Flutter", "Firebase", "Dart", "Charts" , "Google Maps"],
    image: require("@/assets/seadubai.jpeg"),
    demoUrl: "https://play.google.com/store/apps/details?id=com.seadubai.app",
    codeUrl: "#",
  },
  {
    title: "Quality Chauffeur Services",
    description:
      "Experience premium chauffeur services with professionalism and luxury. Our QCS service ensures a smooth and comfortable ride to your destination, whether for business or leisure.",
    technologies: ["Flutter", "Firebase", "Dart", "Google Maps"],
    image: require("@/assets/QCS.jpeg"),
    demoUrl: "https://qcsdrive.com/",
    codeUrl: "#",
  },
  {
    title: "Noir-Cinema",
    description:
      "Noir Cinema brings you the best in classic and modern noir films—mystery, suspense, and style, all in one app.",
    technologies: ["Flutter", "Firebase", "Dart"],
    image: require("@/assets/Noir-Cinema.jpeg"),
    demoUrl: "https://noircinema.sa/en/",
    codeUrl: "#",
  },

  {
    title: "Weather App",
    description:
      "Beautiful weather forecasting application with location-based services.",
    technologies: ["Flutter", "API", "Dart", "Google Maps" , "Weather Api"],
    image: require("@/assets/weatherapp.jpeg"),

    demoUrl: "#",
    codeUrl: "#",
  },
]);

const openProject = (project) => {
  // You can implement a detailed view modal/dialog here
  console.log("Opening project:", project.title);
};
</script>

<style scoped>
.projects-container {
  max-width: 1400px;
  padding-top: 64px;
  padding-bottom: 64px;
}

.project-card {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  height: 100%;
  display: flex;
  flex-direction: column;
}

.project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2) !important;
}

.v-card-actions {
  margin-top: auto;
}
</style>
