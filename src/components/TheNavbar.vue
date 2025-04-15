<template>
  <v-app-bar app density="compact" flat class="mt-2">
    <v-app-bar-nav-icon @click="drawer = !drawer" class="d-md-none">
      <v-icon>mdi-menu</v-icon>
    </v-app-bar-nav-icon>

    <v-app-bar-title>
      <v-btn class="font-weight-bold" variant="plain">Abbas Khan </v-btn>
    </v-app-bar-title>

    <v-spacer></v-spacer>

    <v-toolbar-items class="d-none d-md-flex">
      <v-btn
        :to="{ path: '/', hash: '#home' }"
        density="compact"
        size="small"
        class="mx-2"
        >Home</v-btn
      >
      <v-btn :to="{ path: '/', hash: '#about' }">About</v-btn>
      <v-btn :to="{ path: '/', hash: '#skills' }">Skills</v-btn>
      <v-btn :to="{ path: '/', hash: '#projects' }">Projects</v-btn>
      <v-btn :to="{ path: '/', hash: '#contact' }">Contact</v-btn>
      <v-btn
        href="https://drive.google.com/file/d/136Qn0mujLHyEsLPkrQBpkFFEfEsAirop/view?usp=drive_link"
        target="_blank"
        rel="noopener noreferrer"
        variant="outlined"
        rounded="lg"
        class="text-red"
        >Resume</v-btn
      >

      <v-switch
        v-model="isDark"
        color="red-darken-3"
        @change="toggleTheme"
        base-color="green"
        class="mr-5"
      ></v-switch>
    </v-toolbar-items>
  </v-app-bar>
  <!-- Navigation Drawer for Mobile -->

  <v-navigation-drawer
    :elevation="4"
    v-model="drawer"
    temporary
    class="mt-1"
    width="150"
    style="height: 100vh; position: fixed"
  >
    <v-list>
      <v-list-item
        @click="drawer = false"
        :to="{ path: '/', hash: '#home' }"
        variant="plain"
        >Home</v-list-item
      >
      <v-divider></v-divider>
      <v-list-item
        @click="drawer = false"
        :to="{ path: '/', hash: '#about' }"
        variant="plain"
        >About</v-list-item
      >
      <v-divider></v-divider>
      <v-list-item
        @click="drawer = false"
        :to="{ path: '/', hash: '#skills' }"
        variant="plain"
        >Skills</v-list-item
      >
      <v-divider></v-divider>
      <v-list-item
        @click="drawer = false"
        :to="{ path: '/', hash: '#projects' }"
        variant="plain"
        >Projects</v-list-item
      >
      <v-divider></v-divider>
      <v-list-item
        @click="drawer = false"
        :to="{ path: '/', hash: '#contact' }"
        variant="plain"
        >Contact</v-list-item
      >
      <v-divider></v-divider>
      <v-list-item
        @click="drawer = false"
        href="https://drive.google.com/file/d/136Qn0mujLHyEsLPkrQBpkFFEfEsAirop/view?usp=drive_link"
        target="_blank"
        rel="noopener noreferrer"
        variant="plain"
        rounded="lg"
        >Resume
      </v-list-item>
      <v-divider></v-divider>
      <v-list-item>
        <v-switch
          v-model="isDark"
          color="red-darken-3"
          @change="toggleTheme"
          base-color="green"
        ></v-switch>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script setup>
import { useTheme } from "vuetify/lib/composables/theme";
import { ref, watch } from "vue";

const drawer = ref(false);
const theme = useTheme();
const isDark = ref(theme.global.current.value.dark);

watch(isDark, (newVal) => {
  theme.global.name.value = newVal ? "dark" : "light";
});

function toggleTheme() {
  // Theme automatically updated by watcher
}
</script>

<style scoped>
button:hover,
a:hover {
  background-color: #c62828;
  border-radius: 6px;
}
</style>
