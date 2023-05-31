<script setup lang="ts">
import IconHiGesture from '@/components/Icon/IconHiGesture.vue';
import { useGtm } from '@gtm-support/vue-gtm';
import { onMounted } from 'vue';

const gtm = useGtm();

onMounted(() => {
  triggerEvent();
});

// Generate a random number of 10 digits
const generateRandomId = (): number => {
  const min = 1000000000;
  const max = 9999999999;

  return Math.floor(Math.random() * (max - min + 1)) + min;
};

// const leadId = generateRandomId();

const triggerEvent = () => {
  gtm?.trackEvent({
    event: 'FireGTM',
    leadId: generateRandomId()
  });
};
</script>

<template>
  <div class="d-flex align-items-center justify-content-center">
    <h1>Thank you page</h1>
    <IconHiGesture />
  </div>
</template>
