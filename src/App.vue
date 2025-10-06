<script setup lang="ts">
import { createFormValidityObserver } from "@form-observer/vue";
const observer = createFormValidityObserver("focusout");
</script>

<template>
  <div :ref="(div: HTMLDivElement | null) => console.log(div)"></div>
  <form :ref="observer.autoObserve()">
    <!-- ... -->
  </form>
</template>
