<script setup lang="ts">
import IconStarPlusOutline from "@/components/icons/cards/iconStarPlusOutline.vue";
import IconEye from "@/components/icons/cards/iconEye.vue";
import IconMerge from "@/components/icons/cards/iconMerge.vue";

defineProps<{ title: string; content: string; }>()
</script>

<template>
  <div class="card">
    <h5>{{title}}</h5>
    <p>{{content}}</p>
    <div class="project-buttons">
      <icon-star-plus-outline />
      <icon-eye />
      <icon-merge />
    </div>
  </div>
</template>
