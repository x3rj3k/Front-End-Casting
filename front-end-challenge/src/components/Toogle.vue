<template>
  <Switch
    v-model="enabled"
    :class="enabled ? 'bg-orange-400' : 'bg-gray-400'"
    class="relative inline-flex h-[21px] w-[50px] shrink-0 cursor-pointer rounded-full border-2 border-transparent transition-colors duration-200 ease-in-out focus:outline-none focus-visible:ring-2 focus-visible:ring-white focus-visible:ring-opacity-75"
  >
    <span
      aria-hidden="true"
      :class="enabled ? 'translate-x-7' : 'translate-x-0'"
      class="pointer-events-none inline-block h-[18px] w-[18px] transform rounded-full bg-white shadow-lg ring-0 transition duration-200 ease-in-out"
    />
  </Switch>
</template>
<script setup lang="ts">
import { ref } from 'vue'
import { Switch } from '@headlessui/vue'

const enabled = ref(false)
</script>