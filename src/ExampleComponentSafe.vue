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
  <!-- No error if there are no comments inside -->
  <ul v-if="props.examples.length > 0">
    <li v-for="item in props.examples" :key="item.id">
      {{ item.name }}
    </li>
  </ul>
</template>