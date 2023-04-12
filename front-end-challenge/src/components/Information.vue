<template>
  <div class="w-full mr-20 flex flex-col gap-10">
    <div class="border-2 p-5 rounded-md">
      <div class="flex items-center justify-between -mt-[32px]">
        <span class="bg-white px-2">Verify phone number</span>
        <span class="bg-white px-2"><Toogle /></span>
      </div>
      <div class="flex gap-5">
        <input class="border-2 border-gray-500 rounded-md w-full py-2 mt-5 pl-3" type="text" placeholder="Select country code" />
        <input class="border-2 border-gray-500 rounded-md w-full py-2 mt-5 pl-3" type="number" placeholder="Phone number" />
      </div>
    </div>
    <div class="border-2 p-5 rounded-md">
      <div class="flex items-center justify-between -mt-[32px]">
        <span class="bg-white px-2">Verify email</span>
        <span class="bg-white px-2"><Toogle /></span>
      </div>
      <input class="mt-2 w-full" type="email" placeholder="Email">
    </div>
    <div class="border-2 p-5 rounded-md">
      <div class="flex items-center justify-between -mt-[32px]">
        <span class="bg-white px-2">Verify Identity</span>
        <span class="bg-white px-2"><Toogle /></span>
      </div>
      <span class="flex">Choose an ID type to add <QuestionMarkCircleIcon class="w-5 text-gray-400" /> </span>
      <div class="flex flex-row gap-5 mt-3 border-b-2 pb-7">
        <div class="w-full flex">
          <Menu as="div" class="inline-block text-left w-full">
            <div class="flex gap-5 w-full">
              <MenuButton class="border-2 rounded-md w-full border-gray-400"
              >
              <span class="flex justify-between px-1 text-gray-400 py-1">Issuing country/region <ChevronDownIcon class="w-5" /></span>
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
                class="absolute left-100 mt-2 w-56 origin-top-right divide-y divide-gray-100 rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
              >
                <div class="px-1 py-1">
                  <MenuItem v-slot="{ active }">
                    <button
                      :class="[
                        active ? 'bg-orange-400 text-white' : 'text-gray-900',
                        'group flex w-full items-center rounded-md px-2 py-2 text-sm',
                      ]"
                    >
                      region 1
                    </button>
                  </MenuItem>
                  <MenuItem v-slot="{ active }">
                    <button
                      :class="[
                        active ? 'bg-orange-400 text-white' : 'text-gray-900',
                        'group flex w-full items-center rounded-md px-2 py-2 text-sm',
                      ]"
                    >
                      region 2
                    </button>
                  </MenuItem>
                </div>
              </MenuItems>
            </transition>
          </Menu>
        </div>
        <div class="w-full flex">
          <Menu as="div" class="inline-block text-left w-full">
            <div class="flex gap-5">
              <MenuButton class="border-2 rounded-md w-full border-gray-400"
              >
              <span class="flex justify-between px-1 text-gray-400 py-1">Choose identification <ChevronDownIcon class="w-5" /></span>
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
                class="absolute right-100 mt-2 w-56 origin-top-right divide-y divide-gray-100 rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
              >
                <div class="px-1 py-1">
                  <MenuItem v-slot="{ active }">
                    <button
                      :class="[
                        active ? 'bg-orange-400 text-white' : 'text-gray-900',
                        'group flex w-full items-center rounded-md px-2 py-2 text-sm',
                      ]"
                    >
                      National ID
                    </button>
                  </MenuItem>
                  <MenuItem v-slot="{ active }">
                    <button
                      :class="[
                        active ? 'bg-orange-400 text-white' : 'text-gray-900',
                        'group flex w-full items-center rounded-md px-2 py-2 text-sm',
                      ]"
                    >
                      Valid ID
                    </button>
                  </MenuItem>
                </div>
              </MenuItems>
            </transition>
          </Menu>
        </div>
      </div>
      <span class="flex py-5">Upload images of your ID <QuestionMarkCircleIcon class="w-5 text-gray-400" /> </span>
      <div class="flex gap-5">
        <div class="border-2 w-full p-5 rounded-md justify-center items-center flex flex-col">
          <IdentificationIcon class="w-12" />
          <span>Upload front</span>
          <p>JPEG or PNG only</p>
          <input type="file" id="frontImage" class="hidden" accept=".png, .jpeg"  />
          <label for="frontImage" class="rounded-2xl bg-orange-400 text-white font-semibold px-4 py-1">Select files</label>
        </div>
        <div class="border-2 w-full p-5 rounded-md justify-center items-center flex flex-col">
          <CreditCardIcon class="w-12" />
          <span>Upload back</span>
          <p>JPEG or PNG only</p>
          <input type="file" id="backImage" class="hidden" accept=".png, .jpeg"  />
          <label for="backImage" class="rounded-2xl bg-orange-400 text-white font-semibold px-4 py-1">Select files</label>
        </div>
      </div>
      <div class="border-2 w-full p-5 rounded-md justify-center items-center flex flex-col my-5">
        <ArrowUpTrayIcon class="w-12" />
        <span>Upload picture</span>
        <p>JPEG or PNG only</p>
        <input type="file" id="backImage" class="hidden" accept=".png, .jpeg"  />
        <label for="backImage" class="rounded-2xl bg-orange-400 text-white font-semibold px-4 py-1">Select files</label>
      </div>
    </div>
    <div class="border-t-2 w-full flex justify-end pt-10">
      <button class="rounded-2xl bg-orange-400 text-white font-semibold px-4 py-1">Save & Synchronize</button>
    </div>
  </div>
</template>
<script setup lang="ts">
import { QuestionMarkCircleIcon, ChevronDownIcon } from '@heroicons/vue/24/solid';
import { IdentificationIcon, CreditCardIcon, ArrowUpTrayIcon } from '@heroicons/vue/24/outline'
import { Menu, MenuButton, MenuItems, MenuItem } from '@headlessui/vue'
import Toogle from './Toogle.vue';
</script>
<style scoped>
textarea:focus, input:focus{
    outline: none;
}

/* Chrome, Safari, Edge, Opera */
input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
  margin: 0;
}

/* Firefox */
input[type=number] {
  -moz-appearance: textfield;
}
</style>