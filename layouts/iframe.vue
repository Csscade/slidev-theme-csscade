<!--
  Usage:
```md
---
```yaml
layout: iframe
url: <url>
(optional) scale: <number>
```
-->

<script setup lang="ts">
import { computed } from "vue";
import SlidesCurrentNumber from "../components/slides-current-number.vue";

const props = defineProps<{
  url: string;
  scale?: number;
}>();

const scaleInvertPercent = computed(() => `${(1 / (props.scale || 1)) * 100}%`);
</script>

<template>
  <div class="h-full w-full">
    <div
      relative
      :style="{ width: scaleInvertPercent, height: scaleInvertPercent }"
    >
      <iframe
        id="frame"
        class="w-full h-full"
        :src="url"
        :style="
          scale
            ? { transform: `scale(${scale})`, transformOrigin: 'top left' }
            : {}
        "
      />
    </div>
    <slides-current-number />
  </div>
</template>
