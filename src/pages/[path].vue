<template>
  {{ path }}
</template>

<script lang="ts">
export default definePageComponent({
  getStaticPaths() {
    return ['foobar', 'foo bar'].map((path) => ({
      params: { path },
      props: { path },
    }));
  }
});
</script>

<script setup lang="ts">
const props = defineProps<{
  path: string;
}>();
</script>
