<template>
  <div></div>
</template>

<script lang="ts">
  import { defineComponent, onMounted } from '@vue/composition-api';

  export default defineComponent({
    setup(props: null, { emit }) {
      onMounted(() => {
        emit('ev', true);
      });

      return {};
    }
  });
</script>
