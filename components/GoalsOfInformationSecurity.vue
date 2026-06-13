<template>
  <div
    v-click
    class="fixed top-0 right-0 w-64 h-full bg-gray shadow-2xl transform transition-transform duration-300 p-5"
  >
    <h2 class="text-lg font-bold mb-4">Checkliste der Schutzziele</h2>
    <ul class="space-y-2">
      <li class="flex items-center space-x-2">
        <span v-if="status.confidentiality">✅</span><span v-else>❌</span>
        <span>Vertraulichkeit</span>
      </li>
      <li class="flex items-center space-x-2">
        <span v-if="status.integrity">✅</span><span v-else>❌</span>
        <span>Integrität</span>
      </li>
      <li class="flex items-center space-x-2">
        <span v-if="status.availability">✅</span><span v-else>❌</span>
        <span>Verfügbarkeit</span>
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
const { status } = defineProps<{
  status: {
    confidentiality: boolean;
    integrity: boolean;
    availability: boolean;
  };
}>();
</script>
