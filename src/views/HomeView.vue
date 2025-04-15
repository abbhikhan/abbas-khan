<template>
  <div>
    <!-- Home/Hero Section -->
    <section id="home" class="section">
    <TheHome />  
    </section>

    <!-- About Section -->
    <section id="about" class="section">
    <TheAbout />
    </section>

    <!-- Skills Section -->
    <section id="skills" class="section">
    <TheSkills/>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="section">
    <TheProjects />
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section">
    <TheContact />
    </section>
  </div>
</template>

<script setup>
import TheHome from "@/components/TheHome.vue";
import TheAbout from "@/components/TheAbout.vue";
import TheSkills from "@/components/TheSkills.vue";
import TheProjects from "@/components/TheProjects.vue";
import TheContact from "@/components/TheContact.vue";
// @ is an alias to /src


</script>
