<template>
  <v-container class="contact-container">
    <!-- Header Section -->
    <v-row class="mb-8">
      <v-col cols="12" class="text-center">
        <h1 class="text-h3 font-weight-bold mb-2">Get In Touch</h1>
        <p class="text-subtitle-1 text-grey-darken-1">
          I'd love to hear about your project or opportunity
        </p>
      </v-col>
    </v-row>

    <v-row>
      <!-- Contact Information Column -->
      <v-col cols="12" md="5" class="pe-md-6">
        <v-card variant="flat" class="pa-6 h-100" color="grey-lighten-1">
          <div class="text-center mb-8">
            <v-avatar size="120" class="mb-4">
              <v-img src="@/assets/profile.jpg" alt="Abbas Khan" />
            </v-avatar>
            <h2 class="text-h5 font-weight-bold">Abbas Khan</h2>
            <p class="text-subtitle-1 text-grey-darken-1">Flutter Developer</p>
          </div>

          <!-- Contact Methods -->
          <v-list lines="two" density="comfortable">
            <v-list-item
              prepend-icon="mdi-email"
              href="mailto:Engineer.abaskhan@gmail.com"
            >
              <v-list-item-title>Email</v-list-item-title>
              <v-list-item-subtitle
                >Engineer.abaskhan@gmail.com</v-list-item-subtitle
              >
            </v-list-item>

            <v-list-item prepend-icon="mdi-phone" href="tel:+923149819178">
              <v-list-item-title>Phone</v-list-item-title>
              <v-list-item-subtitle>+92 314 981 9178</v-list-item-subtitle>
            </v-list-item>

            <v-list-item prepend-icon="mdi-map-marker">
              <v-list-item-title>Location</v-list-item-title>
              <v-list-item-subtitle>Islamabad, Pakistan</v-list-item-subtitle>
            </v-list-item>
          </v-list>

          <!-- Social Media Links -->
          <div class="text-center mt-8">
            <v-btn
              v-for="(social, i) in socials"
              :key="i"
              :href="social.url"
              target="_blank"
              icon
              variant="text"
              size="large"
              :color="social.color"
              class="mx-2"
            >
              <v-icon>{{ social.icon }}</v-icon>
              <v-tooltip activator="parent" location="bottom">
                {{ social.name }}
              </v-tooltip>
            </v-btn>
          </div>
        </v-card>
      </v-col>

      <!-- Contact Form Column -->
      <v-col cols="12" md="7">
        <v-card variant="flat" class="pa-6 h-100">
          <h2 class="text-h5 font-weight-bold mb-6">Send Me a Message</h2>
          <v-form @submit.prevent="submitForm">
            <v-row>
              <v-col cols="12" md="6">
                <v-text-field
                  v-model="form.name"
                  label="Your Name"
                  variant="outlined"
                  required
                  :rules="nameRules"
                ></v-text-field>
              </v-col>
              <v-col cols="12" md="6">
                <v-text-field
                  v-model="form.email"
                  label="Email Address"
                  variant="outlined"
                  required
                  :rules="emailRules"
                  type="email"
                ></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field
                  v-model="form.subject"
                  label="Subject"
                  variant="outlined"
                  required
                  :rules="subjectRules"
                ></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-textarea
                  v-model="form.message"
                  label="Your Message"
                  variant="outlined"
                  required
                  :rules="messageRules"
                  rows="4"
                ></v-textarea>
              </v-col>
              <v-col cols="12">
                <v-btn
                  type="submit"
                  color="primary"
                  size="large"
                  :loading="loading"
                >
                  Send Message
                  <v-icon end>mdi-send</v-icon>
                </v-btn>
              </v-col>
            </v-row>
          </v-form>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
import { ref } from "vue";

const socials = [
  {
    icon: "mdi-github",
    color: "grey-darken-3",
    url: "https://github.com/abbhikhan",
    name: "GitHub",
  },
  {
    icon: "mdi-linkedin",
    color: "blue-darken-2",
    url: "https://www.linkedin.com/in/abbhikhan0220?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app",
    name: "LinkedIn",
  },
  {
    icon: "mdi-twitter",
    color: "light-blue",
    url: "https://www.instagram.com/abbhikhann?igsh=czYzcXR4bXFna3Rl",
    name: "Twitter",
  },
  {
    icon: "mdi-facebook",
    color: "blue-darken-3",
    url: "https://www.facebook.com/share/1KyJhfgWvo/",
    name: "Facebook",
  },
];

const form = ref({
  name: "",
  email: "",
  subject: "",
  message: "",
});

const loading = ref(false);

const nameRules = [
  (v) => !!v || "Name is required",
  (v) => v.length >= 3 || "Name must be at least 3 characters",
];

const emailRules = [
  (v) => !!v || "Email is required",
  (v) => /.+@.+\..+/.test(v) || "Email must be valid",
];

const subjectRules = [
  (v) => !!v || "Subject is required",
  (v) => v.length >= 5 || "Subject must be at least 5 characters",
];

const messageRules = [
  (v) => !!v || "Message is required",
  (v) => v.length >= 10 || "Message must be at least 10 characters",
];

const submitForm = () => {
  loading.value = true;
  // Simulate form submission
  setTimeout(() => {
    console.log("Form submitted:", form.value);
    loading.value = false;
    // Reset form after submission
    form.value = { name: "", email: "", subject: "", message: "" };
  }, 1500);
};
</script>

<style scoped>
.contact-container {
  max-width: 1200px;
  padding-top: 64px;
  padding-bottom: 64px;
}

.h-100 {
  height: 100%;
}
</style>
