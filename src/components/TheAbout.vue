<template>
  <v-container class="about-section">
    <v-row align="center" class="my-2">
      <!-- Image Column (Left) -->
      <v-col cols="12" md="5" class="text-center">
        <v-avatar size="300" rounded="0">
          <v-img :src="require('@/assets/aboutMe.jpeg')" alt="Abbas Khan" >
            <template v-slot:placeholder>
              <v-row align="center" class="fill-height ma-0" justify="center">
                <v-progress-circular
                  color="grey-lighten-5"
                  indeterminate
                ></v-progress-circular>
              </v-row>
            </template>
          </v-img>
        </v-avatar>
      </v-col>

      <!-- Text Column (Right) -->
      <v-col cols="12" md="7">
        <h2 class="text-h4 font-weight-bold mb-4">About Me</h2>
        <p class="text-subtitle-1 mb-6">Get to know me )</p>

        <h3 class="text-h5 font-weight-bold mb-3">Who am I?</h3>
        <p class="text-body-1 mb-4">
          I'm <span class="font-weight-bold">Abbas Khan</span>, a Flutter
          developer.
        </p>

        <p class="text-body-1 mb-4">
          A passionate Flutter Developer with a degree in Computer Software
          Engineering from UET Mardan. With nearly 3 years of hands-on
          experience in mobile app development, I specialize in building
          high-quality, cross-platform applications using Flutter. I take pride
          in writing clean, maintainable code and crafting smooth user
          experiences. Whether it’s building apps from scratch or optimizing
          existing projects, I enjoy turning ideas into functional, beautiful
          mobile applications. I’m always eager to learn new technologies and
          take on challenging projects that help me grow as a developer.
        </p>

        <h3 class="text-h5 font-weight-bold mb-3">
          Technologies I have worked with:
        </h3>
        <div class="d-flex flex-wrap ga-2 mb-6 justify-center">
          <v-chip variant="outlined" color="primary">Flutter</v-chip>
          <v-chip variant="outlined" color="primary">Dart</v-chip>
          <v-chip variant="outlined" color="primary">Flutter Web</v-chip>
          <v-chip variant="outlined" color="primary">Flutter Desktop</v-chip>
          <v-chip variant="outlined" color="primary">Flutter Fire</v-chip>
          <v-chip variant="outlined" color="primary">GetX</v-chip>
          <v-chip variant="outlined" color="primary">FCM</v-chip>
          <v-chip variant="outlined" color="primary">Apis</v-chip>

          <v-chip variant="outlined" color="primary">C++</v-chip>
        </div>

        <div class="contact-info">
          <p class="text-body-1 mb-1">
            <span class="font-weight-bold">Name:</span> Abbas Khan
          </p>
          <p class="text-body-1">
            <span class="font-weight-bold">Email:</span>
            Engineer.abaskhan@gmail.com
          </p>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
// No script needed for basic implementation
</script>

<style scoped>
.about-section {
  max-width: 1200px;
}

@media (max-width: 960px) {
  .about-section {
    text-align: center;
  }
  .contact-info {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}
</style>
