<template>
      <div class="w-full gradient-blue flex flex-col md:flex-row py-6">
        <div
      class="w-full container mx-auto flex flex-wrap items-center justify-between mt-0 py-2"
    >
          <p class="uppercase text-gray-500 md:mb-6">Links</p>
          <ul class="list-reset mb-6">
            <li class="mt-2 inline-block mr-2 md:block md:mr-0">
              <a
                href="#"
                class="no-underline hover:underline text-gray-800 hover:text-pink-500"
                >Template from github</a
              >
            </li>
          </ul>
          <p class="uppercase text-gray-500 md:mb-6"></p>
          <ul>
            <a class="z-50 bottom-6 left-2" title="Free source codes" href="https://github.com/hakimov-dev/landing-template" target="_blank">
              <img class="!h-12"   src="../../assets/imgs/github.svg" alt="github">
            </a>
          </ul>
          <p class="uppercase text-gray-500 md:mb-6"></p>
          <ul>
            <a class="z-50 bottom-6 right-2" title="Support me" href="https://www.buymeacoffee.com/hakimovDev" target="_blank">
              <img class="!h-12" src="../../assets/imgs/buy-me-coffe.png" alt="Buy me a coffe">
            </a>
          </ul>
        </div>
      </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "layout-footer",
});
</script>
