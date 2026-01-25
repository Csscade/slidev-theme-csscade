<!--
  Usage:
```md
---
```yaml
layout: statement
(optional) slogan: <your slogan>
```

### <big concept>

<subtitle>
-->

<script setup lang="ts">
import BigConcept from "../components/big-concept.vue";
import SlidesCurrentNumber from "../components/slides-current-number.vue";

const props = defineProps({
  slogan: {
    type: String,
  },
});
</script>

<template>
  <section class="slidev-layout statement">
    <div>
      <big-concept :slogan="slogan" />
      <slot />
    </div>
    <slides-current-number />
  </section>
</template>

<style>
.slidev-layout.statement {
  padding: 1.5rem 5rem 6rem;
  text-align: center;

  h3 {
    font-size: 3rem;
    line-height: 3rem;
    margin-bottom: 1.5rem;
  }

  p {
    margin: auto;
    max-width: 80%;
  }
}
</style>
