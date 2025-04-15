<template>
  <v-container
    fluid
    class="fill-height d-flex align-center justify-center mt-md-5"
  >
    <v-row justify="center" class="mt-md-5">
      <v-col cols="12" md="6" class="text-center">
        <!-- Welcome text -->
        <div
          class="text-h6 text-md-h5 text-grey-darken-1 font-weight-light letter-spacing-4 text-uppercase my-8"
        >
          WELCOME TO MY PORTFOLIO!
          <span class="wave-emoji">👋</span>
        </div>

        <!-- Name with line break -->
        <h1 class="text-h4 text-md-h2 font-weight-regular line-height-1 mb-4">
          Abbas
        </h1>
        <h1 class="text-h2 text-md-h2 font-weight-bold line-height-1 mb-4">
          Khan
        </h1>

        <!-- Subtitle -->
        <div
          class="text-body-1 text-md-h6 text-grey-darken-2 d-flex align-center justify-center"
        >
          <v-icon color="red-lighten-1" size="small" class="mr-2"
            >mdi-heart</v-icon
          >
          A friend :)
          <span class="ml-3" ref="typedElement"></span>
        </div>

        <v-container>
          <v-row justify="center" class="my-4">
            <v-col cols="auto" v-for="(social, i) in socials" :key="i">
              <v-btn
                icon
                variant="text"
                :color="social.color"
                :href="social.url"
                target="_blank"
                size="x-large"
              >
                <v-icon>{{ social.icon }}</v-icon>
                <v-tooltip activator="parent" location="bottom">
                  {{ social.name }}
                </v-tooltip>
              </v-btn>
            </v-col>
          </v-row>
        </v-container>
      </v-col>

      <v-col cols="12" md="6" class="d-flex align-center justify-center">
        <v-avatar size="300" rounded="cicle">
          <v-img
            :src="require('@/assets/profile.jpeg')"
            alt="Profile Image"
            cover
            class="align-center"
          >
          <template v-slot:placeholder>
          <v-row
            align="center"
            class="fill-height ma-0"
            justify="center"
          >
            <v-progress-circular
              color="grey-lighten-5"
              indeterminate
            ></v-progress-circular>
          </v-row>
        </template></v-img>
        </v-avatar>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import Typed from 'typed.js';

const typedElement = ref(null);

onMounted(() => {
  new Typed(typedElement.value, {
    strings: [' a Flutter Developer', 'QA Specialist', 'a Freelancer','a Programmer'], // Texts to cycle through
    typeSpeed: 100, // Typing speed (ms)
    backSpeed: 80, // Backspacing speed (ms)
    loop: true, // Infinite loop
  });
});
const socials = [
  {
    icon: "mdi-facebook",
    color: "blue-darken-3",
    url: "https://www.facebook.com/share/1KyJhfgWvo/",
    name: "Facebook",
  },
  {
    icon: "mdi-instagram",
    color: "pink-darken-1",
    url: "https://www.instagram.com/abbhikhann?igsh=czYzcXR4bXFna3Rl",
    name: "Instagram",
  },
  {
    icon: "mdi-twitter",
    color: "light-blue",
    url: "https://www.instagram.com/abbhikhann?igsh=czYzcXR4bXFna3Rl",
    name: "Twitter",
  },
  {
    icon: "mdi-linkedin",
    color: "blue-darken-2",
    url: "https://www.linkedin.com/in/abbhikhan0220?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app",
    name: "LinkedIn",
  },
  {
    icon: "mdi-github",
    color: "grey-darken-3",
    url: "https://github.com/abbhikhan",
    name: "GitHub",
  },
];
</script>
<style scoped>
/* Minimal animation CSS */
.wave-emoji {
  display: inline-block;
  animation: wave 2s infinite;
  transform-origin: 70% 70%;
  font-size: 1.2em;
  margin-left: 0.3rem;
}

@keyframes wave {
  0% {
    transform: rotate(0deg);
  }
  10% {
    transform: rotate(-10deg);
  }
  20% {
    transform: rotate(12deg);
  }
  30% {
    transform: rotate(-10deg);
  }
  40% {
    transform: rotate(9deg);
  }
  50% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(0deg);
  }
}
</style>
