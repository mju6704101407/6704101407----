<template>
  <q-page class="flex flex-center">
    <q-form @submit.prevent="onSubmit" class="q-gutter-md">
      <q-input filled label="Name" v-model="form.name" />
      <q-input filled label="Email" v-model="form.email" type="email" />
      <q-btn type="submit" label="Submit" color="primary" />
    </q-form>
  </q-page>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const form = ref({ name: '', email: '' })

function onSubmit() {
  console.log('Form submitted', form.value)
}
</script>
