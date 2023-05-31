<script setup lang="ts">
interface Props {
  height?: number;
  width?: number;
}
withDefaults(defineProps<Props>(), {
  height: 800,
  width: 800
});
</script>

<template>
  <svg :width="width" :height="height" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
    <path
      d="M4 21v-2.5A5.5 5.5 0 0 1 9.5 13h3.351a5.5 5.5 0 0 0 5.289-3.989l.605-2.12a1.228 1.228 0 0 1 2.373.635l-1.754 7.019A1.921 1.921 0 0 1 17.5 16M8 21v-3m8-11.5a4 4 0 1 1-8 0 4 4 0 0 1 8 0Z"
      stroke="#000"
      stroke-linecap="round"
      stroke-width="1.4"
    />
  </svg>
</template>
