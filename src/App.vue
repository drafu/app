<template>
  <div>
    <A :pattern="/./"/>

    <div
      class="file"
      v-for="(k, v) in o.v"
      :key="v"
    >{{v}}</div>

    <B @ev="(v) => { o = v; }"/>
  </div>
</template>

<script lang="ts">
  import { defineComponent, ref, SetupContext, Ref } from '@vue/composition-api';

  import A from './components/A.vue';
  import B from './components/B.vue';

  export default defineComponent({
    components: {
      A,
      B
    },
    setup(props: null, { emit }: SetupContext) {
      const o: Ref<boolean[]> = ref([false]);

      return {
        o,
        emit
      };
    }
  });
</script>
