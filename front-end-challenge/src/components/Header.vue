<template>
  <div>
    <div class="flex justify-between px-20">
      <h1 class="text-3xl font-black flex w-full">Spondise <PlayIcon class="w-6 -ml-11 -mt-7 text-orange-400" /></h1>
      <div class="flex border-2 rounded-md w-full border-gray-400 shadow-md">
        <span class="flex items-center justify-between border-r-2 px-2 border-gray-400 w-full">Filter <AdjustmentsHorizontalIcon class="w-5" /> </span>
        <span class="flex items-center w-full justify-between px-2">Smart Search <MagnifyingGlassIcon class="w-5" /></span>
      </div>
      <div class="w-full flex justify-end">
        <Menu as="div" class="inline-block text-left">
          <div class="flex gap-5">
            <div class="flex gap-2">
              <DocumentTextIcon class="w-8" />
              <BellIcon class="w-8" />
              <EnvelopeIcon class="w-8" />
            </div>
            <MenuButton class="border-2 rounded-full w-fit border-gray-400"
            >
            <span class="flex items-center pl-5"> <p class="flex flex-col justify-center items-center">Sponsor <ChevronDownIcon class="w-4" /></p> <img :src="UserImage" class="h-10 w-10 ml-4 rounded-full" alt="User Image" /></span>
            <span class="flex absolute rounded-full bg-blue-400 text-white px-1 ml-[120px] -mt-5 border-2 border-white">57</span>
            </MenuButton>
          </div>
          <transition
            enter-active-class="transition duration-100 ease-out"
            enter-from-class="transform scale-95 opacity-0"
            enter-to-class="transform scale-100 opacity-100"
            leave-active-class="transition duration-75 ease-in"
            leave-from-class="transform scale-100 opacity-100"
            leave-to-class="transform scale-95 opacity-0"
          >
            <MenuItems
              class="absolute right-20 mt-2 w-56 origin-top-right divide-y divide-gray-100 rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
            >
              <div class="px-1 py-1">
                <MenuItem v-slot="{ active }">
                  <button
                    :class="[
                      active ? 'bg-orange-400 text-white' : 'text-gray-900',
                      'group flex w-full items-center rounded-md px-2 py-2 text-sm',
                    ]"
                  >
                    Dropdown 1
                  </button>
                </MenuItem>
                <MenuItem v-slot="{ active }">
                  <button
                    :class="[
                      active ? 'bg-orange-400 text-white' : 'text-gray-900',
                      'group flex w-full items-center rounded-md px-2 py-2 text-sm',
                    ]"
                  >
                    Drowpdown 2
                  </button>
                </MenuItem>
              </div>
            </MenuItems>
          </transition>
        </Menu>
      </div>
    </div>
    <div class="border-t-2 border-b-2 flex justify-between px-20 mt-5 mb-10 py-4">
      <span class="text-orange-400 w-full">Dashboard > Sponsor Profile > Verification</span>
      <span class="w-full flex gap-5 items-center justify-center">Sponsor <Toogle /> Creator</span>
      <div class="flex flex-col gap-1 w-full">
        <div class="flex flex-row items-center justify-between text-sm text-dark-gray pl-48">
          <span class="flex justify-between w-full">Profile Completeness <p>90%</p></span>
        </div>
        <div class="h-[10px] rounded-md bg-gray-100 overflow-hidden ml-48">
          <div class="bg-orange-400 h-full" :style="{ width: `90%` }"></div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import { AdjustmentsHorizontalIcon, MagnifyingGlassIcon, DocumentTextIcon, BellIcon, EnvelopeIcon } from '@heroicons/vue/24/outline'
import { PlayIcon, ChevronDownIcon } from '@heroicons/vue/24/solid'
import { Menu, MenuButton, MenuItems, MenuItem } from '@headlessui/vue'

import Toogle from './Toogle.vue'

import UserImage from '@/assets/images/first-person.png'
</script>
