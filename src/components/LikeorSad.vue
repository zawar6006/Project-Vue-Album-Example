<template>
  <div class="btn-group">
    <button type="button" class="btn btn-sm btn-outline-success" @click="ilike">
      <i class="bi bi-emoji-smile"></i>
      {{ likes }} 
    </button>
    <button type="button" class="btn btn-sm btn-outline-danger" @click="isad">
      <i class="bi bi-emoji-frown"></i>
      {{ sads }} 
    </button>
  </div>
</template>
<script setup>
import { ref } from "vue";
let [likes, sads] = [ref(0), ref(0)];
function ilike() {
  return likes.value++;
}
function isad() {
  return sads.value++;
}
</script>
<style scoped></style>
