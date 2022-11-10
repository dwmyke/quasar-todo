<template>
   <q-page class="flex flex-center" padding>
    <q-card class="full-width" style="max-width: 450px">
      <q-card-section class="text-center" style="font-size: 1.3em">
        Contact Mike
      </q-card-section>
      <q-card-section>
        <q-input
        v-model="form.email"
        filled
        label="Email Address"
        class="q-mb-md"
        />
        <q-input
        v-model="form.message"
        filled
        label="Message"
        />
      </q-card-section>

      <q-btn
      class="full-width"
      label="Send"
      color="primary"
      @click="send"
      />
    </q-card>
  </q-page>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'
export default defineComponent({
   name: 'ContactPage',
   setup () {
    const form = ref({
      email: '',
      message: ''
    });

    function send() {
      console.log(form.value)
    }
    return { form, send };
   },
})
</script>
