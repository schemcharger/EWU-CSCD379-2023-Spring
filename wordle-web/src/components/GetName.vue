<template>
  <v-btn flat @click="setOverlay">{{ name }}</v-btn>
  <v-dialog v-model="overlay" persistent class="w-25">
    <v-card>
      <v-text-field v-model="name" label="Name" />
      <v-btn @click="setOverlay">close</v-btn>
    </v-card>
  </v-dialog>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const name = ref('Guest')

const overlay = ref(false)

const emits = defineEmits<{
  (event: 'overlay', value: string): void
}>()

function setOverlay() {
  overlay.value = !overlay.value
  emits('overlay', name.value)
}
</script>
