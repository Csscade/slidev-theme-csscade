<!--
  Usage:
```md
---
```yaml
layout: default
```

<content>
-->
<script setup lang="ts">
import SlidesCurrentNumber from "../components/slides-current-number.vue";
</script>

<template>
  <section class="slidev-layout default">
    <article>
      <slot />
    </article>
  </section>
  <slides-current-number />
</template>

<style>
.slidev-layout.default {
  padding: 7.5rem 8rem 6rem;

  h3 {
    font-size: 3rem;
    line-height: 3rem;
    margin-bottom: 40px;
  }
}
</style>
