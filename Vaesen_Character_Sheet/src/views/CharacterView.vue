<template>
  <main>
    <h1>This is a character sheet</h1>
    <CharacterDetails />
    <v-card>
        <ul>
        <li>add details</li>
        <li>add portrait</li>
        <li>add attributes</li>
        <li>add conditions</li>
        <li>add skills</li>
        <li>add talents</li>
        <li>add insights/defects</li>
        <li>add Advantages</li>
        <li>add equipment</li>
        <li>add notes</li>
        </ul>
    </v-card>
  </main>
</template>

<script setup lang="ts">
import CharacterDetails from "@/components/CharacterDetails.vue";
</script>
