<script setup lang="ts">
import type { FormSubmitEvent } from '#ui/types'
import { reactive } from 'vue';

const state = reactive({
  firstname: undefined,
  lastname: undefined,
  street: undefined,
  streetNumber: undefined,
})

async function onSubmit (event: FormSubmitEvent<any>) {
  // Do something with data
  console.log(event.data)
}
</script>

<template>
  <UForm :state="state" class="space-y-4 w-64 p-4 shadow" @submit="onSubmit">
    <UFormGroup label="Firstname" name="firstname">
      <UInput v-model="state.firstname" />
    </UFormGroup>

    <UFormGroup label="Lastname" name="lastname">
      <UInput v-model="state.lastname" />
    </UFormGroup>

    <UFormGroup label="Street" name="street">
      <UInput v-model="state.street" />
    </UFormGroup>

    <UFormGroup label="Street number" name="streetNumber">
      <UInput v-model="state.streetNumber" type="number"/>
    </UFormGroup>

    <UButton type="submit">
      Submit
    </UButton>
  </UForm>
</template>

