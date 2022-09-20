<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  props: {
    msg: { type: String },
  },

  setup() {
    function foo() {
      return "bar";
    }

    return {
      foo,
    };
  },

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
