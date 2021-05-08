<template>
  <v-switch class="mt-6" inset v-model="theme" :prepend-icon="themeIcon"></v-switch>
</template>

<script>
export default {
  data() {
    return {
      theme: true,
    };
  },
  computed: {
    themeIcon() {
      return this.theme ? "mdi-weather-night" : "mdi-weather-sunny";
    },
  },
  watch: {
    theme() {
      this.$vuetify.theme.dark = this.theme;
    },
  },
};
</script>