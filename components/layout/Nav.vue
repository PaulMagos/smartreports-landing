<template>
  <nav id="header" class="fixed w-full z-30 top-0 text-white">
    <div
      class="w-full container mx-auto flex flex-wrap items-center justify-between mt-0 py-2"
    >
      <div id="logo_" class="pl-4 flex items-center">
        <svg version="1.0" xmlns="http://www.w3.org/2000/svg"
           width="90px" viewBox="0 0   1672.000000 794.000000"
           preserveAspectRatio="xMidYMid meet">
          <g transform="translate(0.000000,794.000000) scale(0.100000,-0.100000)"
          fill="#000000" stroke="none">
          <path d="M11410 6624 c0 -3 413 -616 918 -1361 504 -746 921 -1364 925 -1373
          7 -13 -209 -344 -953 -1460 -529 -793 -964 -1448 -967 -1456 -4 -12 72 -14
          500 -14 441 0 506 2 517 15 7 9 333 500 724 1091 391 592 715 1076 721 1077 5
          0 334 -490 730 -1089 l720 -1089 509 -3 c433 -2 507 0 503 12 -3 8 -438 662
          -966 1455 -529 792 -961 1444 -961 1447 0 6 1722 2557 1817 2692 l44 62 -513
          0 -513 -1 -681 -1012 c-374 -556 -684 -1012 -689 -1011 -5 1 -316 456 -690
          1012 l-680 1012 -507 0 c-280 0 -508 -3 -508 -6z m893 -241 c8 -10 345 -509
          749 -1108 403 -600 738 -1091 743 -1091 6 0 336 484 733 1075 398 592 735
          1091 748 1109 l25 32 220 0 c120 0 219 -3 219 -6 0 -3 -382 -571 -849 -1261
          l-849 -1255 889 -1334 c489 -734 889 -1336 889 -1339 0 -3 -101 -5 -224 -5
          l-223 0 -785 1186 c-431 653 -787 1187 -792 1188 -4 1 -361 -533 -793 -1186
          l-785 -1188 -225 0 c-177 0 -223 3 -217 13 4 6 404 606 888 1332 483 726 879
          1325 879 1331 0 5 -381 573 -846 1262 -466 688 -847 1253 -847 1256 0 4 98 6
          218 6 196 0 221 -2 235 -17z"/>
          <path d="M308 5544 c-5 -4 -8 -754 -8 -1666 l0 -1658 624 0 c677 0 758 5 945
          55 256 69 446 180 626 366 215 222 343 507 402 889 21 143 24 527 4 670 -93
          681 -438 1117 -1014 1284 -189 55 -240 58 -932 63 -352 3 -643 1 -647 -3z
          m1272 -364 c227 -30 415 -116 563 -259 271 -261 394 -657 366 -1178 -31 -561
          -298 -975 -719 -1112 -150 -49 -192 -52 -647 -58 l-433 -5 0 1311 0 1311 398
          0 c218 0 431 -5 472 -10z"/>
          <path d="M4409 5523 c-6 -16 -287 -757 -624 -1648 -338 -891 -617 -1628 -620
          -1638 -7 -16 5 -17 196 -15 l202 3 153 410 153 410 773 3 773 2 154 -415 155
          -415 202 0 202 0 -37 98 c-21 53 -305 802 -631 1665 l-593 1567 -224 0 -223 0
          -11 -27z m548 -1255 c166 -453 305 -831 308 -840 7 -17 -27 -18 -619 -18 -344
          0 -626 4 -626 8 0 6 474 1307 605 1660 2 6 10 12 18 12 9 0 119 -288 314 -822z"/>
          <path d="M6250 5370 l0 -180 535 0 535 0 0 -1485 0 -1485 200 0 200 0 0 1485
          0 1485 535 0 535 0 0 180 0 180 -1270 0 -1270 0 0 -180z"/>
          <path d="M10165 5533 c-7 -18 -1185 -3130 -1231 -3250 l-23 -63 202 0 202 0
          154 415 154 415 772 0 773 0 135 -362 c74 -200 143 -387 153 -415 l19 -53 202
          0 202 0 -13 38 c-15 41 -1170 3091 -1218 3215 l-29 77 -224 0 c-203 0 -223 -2
          -230 -17z m250 -460 c25 -64 605 -1653 605 -1657 0 -3 -281 -6 -625 -6 -344 0
          -625 2 -625 5 0 2 133 368 296 812 163 444 301 820 306 836 11 31 32 36 43 10z"/>
          </g>
          </svg>
      </div>
      <div class="block lg:hidden pr-4">
        <button
          @click="mobileSidebar = !mobileSidebar"
          id="nav-toggle"
          class="flex items-center p-1 text-pink-800 hover:text-gray-900 focus:outline-none focus:shadow-outline transform transition hover:scale-105 duration-300 ease-in-out"
        >
          <svg
            class="fill-current h-6 w-6"
            viewBox="0 0 20 20"
            xmlns="http://www.w3.org/2000/svg"
          >
            <title>Menu</title>
            <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
          </svg>
        </button>
      </div>
      <div
        :class="mobileSidebar ? '' : 'hidden'"
        class="w-full flex-grow lg:flex lg:items-center lg:w-auto mt-2 lg:mt-0 bg-white lg:bg-transparent text-black p-4 lg:p-0 z-20"
        id="nav-content"
      >
        <ul class="list-reset lg:flex justify-end flex-1 items-center">
          <li class="mr-3">
            <a
              class="inline-block uppercase py-2 px-4 font-medium no-underline"
              href="#"
              >Home</a
            >
          </li>
          <li class="mr-3">
            <a
              class="inline-block uppercase no-underline font-medium hover:text-gray-800 hover:text-underline py-2 px-4"
              href="#history"
              >History</a
            >
          </li>
          <li class="mr-3">
            <a
              class="inline-block uppercase no-underline font-medium hover:text-gray-800 hover:text-underline py-2 px-4"
              href="#improve"
              >Improve</a
            >
          </li>
          <li class="mr-3">
            <a
              class="inline-block uppercase no-underline font-medium hover:text-gray-800 hover:text-underline py-2 px-4"
              href="#feedback"
              >Feedback</a
            >
          </li>
          <li class="mr-3">
            <a
              class="inline-block uppercase no-underline font-medium hover:text-gray-800 hover:text-underline py-2 px-4"
              href="#subfeedback"
              >other Feedback</a
            >
          </li>
          <li class="mr-3">
            <a
              class="inline-block uppercase no-underline font-medium hover:text-gray-800 hover:text-underline py-2 px-4"
              href="#customers"
              >Customers</a
            >
          </li>
          <li class="mr-3">
            <a
              class="inline-block uppercase no-underline font-medium hover:text-gray-800 hover:text-underline py-2 px-4"
              href="#access"
              >Access</a
            >
          </li>
          <li class="mr-3">
            <a
              class="inline-block uppercase no-underline font-medium hover:text-gray-800 hover:text-underline py-2 px-4"
              href="#contact"
              >About Us</a
            >
          </li>
        </ul>
        <!-- <button
          id="navAction"
          class="mx-auto lg:mx-0 hover:underline bg-white text-gray-800 font-bold rounded-full mt-4 lg:mt-0 py-4 px-8 shadow opacity-75 focus:outline-none focus:shadow-outline transform transition hover:scale-105 duration-300 ease-in-out"
        >
          Action
        </button> -->
      </div>
    </div>
    <hr class="border-b border-gray-100 opacity-25 my-0 py-0" />
  </nav>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "layout-nav",
  data() {
    return {
      scrollY: 0,
      mobileSidebar: false,
    };
  },
  mounted() {
    this.scrollY = window.scrollY;

    // Listen to the scroll event to update the scrollY property dynamically
    window.addEventListener("scroll", this.handleScroll);
  },

  methods: {
    handleScroll() {
      this.scrollY = window.scrollY;
    },
  },

  watch: {
    scrollY(newValue: number) {
      var navaction = document.getElementById("navAction");
      var my_logo = document.getElementById("logo_");
      var header = document.getElementById("header");
      var toToggle = document.querySelector(".toggleColour");
      if (newValue > 10) {
        my_logo?.classList.remove("invert-color");
        navaction?.classList.remove("bg-white");
        navaction?.classList.add("gradient-blue-button");
        navaction?.classList.remove("text-[#170F4F]");
        navaction?.classList.add("text-white");
        header?.classList.add("bg-white");
        header?.classList.add("navbar-active");
        toToggle?.classList.add("text-gray-800");
        toToggle?.classList.remove("text-white");
      } else {
        my_logo?.classList.add("invert-color");
        navaction?.classList.add("bg-white");
        navaction?.classList.remove("gradient-blue-button");
        navaction?.classList.add("text-[#170F4F]");
        navaction?.classList.remove("text-white");
        header?.classList.remove("bg-white");
        header?.classList.remove("navbar-active");
        toToggle?.classList.remove("text-gray-800");
        toToggle?.classList.add("text-white");
      }
    },
  },
});
</script>

<style>
a {
  font-weight: 600;
  font-style: normal !important;
  color: white;
}

.navbar-active ul li a{
  color: #170F4F;
}

.invert-color {
  filter: invert(1);
}
</style>
