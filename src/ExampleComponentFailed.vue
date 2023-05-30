<script setup lang="ts">
export type ExampleComponentProps = {
  examples: {
    id: number;
    name: string;
  }[];
};

const props = defineProps<ExampleComponentProps>();
</script>

<template>
  <ul v-if="props.examples.length > 0">
    <!-- Error if comment inserted inside ul element -->
    <li v-for="item in props.examples" :key="item.id">
      {{ item.name }}
    </li>
  </ul>
</template>