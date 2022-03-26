<template>
  <a
    :href="props.url"
    class="grid place-content-center bg-black text-white px-3 py-2 m-4 rounded-lg"
    ><slot></slot
  ></a>
</template>

<script setup>
import {defineProps} from 'vue';

const props = defineProps({
  url: {
    type: String,
  },
});
</script>