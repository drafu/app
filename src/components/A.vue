<template>
  <div></div>
</template>

<script lang="ts">
  import { defineComponent } from '@vue/composition-api';

  interface Props {
    pattern: RegExp;
  }

  export default defineComponent({
    props: {
      pattern: {
        type: RegExp,
        required: true
      }
    },
    setup(props: Props) {
      return {
        props
      };
    }
  });
</script>
