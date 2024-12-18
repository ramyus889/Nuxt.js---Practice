<script setup lang="ts">


const count = ref(0);

const { width } = useWindowSize();

const isMobile = computed(() => width.value < 768);
</script>

<template>
  <div class="inline-flex flex-col gap-2">
    <div class="">Frontend count: {{ count }}</div>
    <UseButton
      label="Click"
      motion-animate="m-p-wobble"
      bg-color="bg-green"
      :size="isMobile ? 'medium' : 'large'"
      @click="count++"
    />
  </div>
</template>
