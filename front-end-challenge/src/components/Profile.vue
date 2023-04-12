<template>
  <div class="w-1/2 border-2 p-8 ml-20 rounded-lg h-fit">
    <div class="flex flex-col items-center gap-2 pb-7">
      <img :src="UserImage" class="rounded-full w-40 h-40" alt="Users" />
      <span class="text-xl font-normal flex gap-3">Jhonny_Official <PencilIcon class="w-5" /></span>
    </div>
    <ul class="flex flex-col gap-5">
      <li class="flex justify-between border-t-2 pt-3">Sponsor Level <span class="flex rounded-full bg-blue-400 text-white px-1">57</span></li>
      <li class="flex justify-between border-t-2 pt-3">Sponsor Plan <span class="flex gap-1">Platinum <TrophyIcon class="w-6 h-6 px-1 bg-blue-400 text-white rounded-full" /></span></li>
      <li class="flex justify-between border-t-2 pt-3">Verified <span class="rounded-full bg-red-700 flex px-[2px]"><XMarkIcon class="w-5 text-white" /></span></li>
      <li class="flex justify-between border-t-2 pt-3">Ratings <span class="flex gap-1"><StarIcon class="w-5"/> 5.0</span></li>
      <li class="flex justify-between border-t-2 border-b-2 py-3">Completed Contracts <span>14</span></li>
    </ul>
  </div>
</template>
<script setup lang="ts">
import { PencilIcon, TrophyIcon, StarIcon, XMarkIcon } from '@heroicons/vue/24/outline';
import UserImage from '@/assets/images/first-person.png'
</script>