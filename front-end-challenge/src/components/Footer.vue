<template>
  <div class="flex justify-between px-10 shadow-md py-5 border-t-2 mt-10">
    <span>© 2023 - All rights reserved</span>
    <ul class="flex space-x-10">
      <li class="list-disc" v-for="footerData in data" :key="`${footerData}`">
        {{ footerData }}
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
const data = ['Compensation data', 'Affiliaties', 'Contact Us', 'Support', 'Our Partners', 'Team']
</script>

<style scoped>
li:first-child {
  list-style: none
}
</style>