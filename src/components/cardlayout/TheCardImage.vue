<template>
<div class="flex justify-center">
  <img
    :src="props.url"
    :alt="props.alt"
    class="h-24 w- object-cover rounded-t-md my-1"
  />
</div>
</template>
<script setup>
import {defineProps} from 'vue';

  const props = defineProps({
    url: {
      type: String,
      required: true,
    },
    alt: {
      type: String,
    },
  });
</script>