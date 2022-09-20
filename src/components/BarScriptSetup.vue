<script setup lang="ts">
function foo() {
  return "bar";
}

defineExpose({
  foo,
});
</script>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  methods: {
    bar() {
      return this.foo();
    },
  },
});
</script>

<template>
  <div>Bar: {{ bar() }}</div>
</template>
