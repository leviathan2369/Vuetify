<template>
   <v-app>
      <CardPrinter />
    </v-app>
</template>

<script>
import CardPrinter from './components/CardPrinter.vue'

export default {
  name: 'App',
  components: {
    CardPrinter
  }
}
</script>

<style>
@import "https://cdn.jsdelivr.net/npm/tailwindcss@latest/dist/tailwind.min.css";
</style>
