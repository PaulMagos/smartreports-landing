<!-- GroupMembers.vue -->
<template>
  <div class="container mx-auto w-5/6  px-2 pt-4 pb-12 text-gray-800">
    
    <div class="container m-8">
      <h2
      class="w-full my-2 text-8xl font-bold leading-tight text-center text-gray-800"
      >
      About Us
    </h2>
  </div><div
  data-aos="fade-up-left"
  class="flex flex-wrap flex-col-reverse sm:flex-row members-container">
  <MemberCard
  v-for="(member, index) in groupMembers"
  :key="index"
  :name="member.name"
  :role="member.role"
  :groups="member.groups"
  :avatar="member.avatar"
  />
</div>
</div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import MemberCard from "./MemberCard.vue"; // Create MemberCard.vue separately
import type { variants } from "~/tailwind.config";

export default defineComponent({
  name: "GroupMembers",
  data() {
    return {
      groupMembers: [
        { name: "Paul Magos", role: "Project Manager", groups: {"UX": 'primary', "Back End": 'yellow', "Front End": 'fuchsia'}, avatar: "paul.jpeg"},
        {
    name: "Samuele Bonini",
    role: "Head of Front End",
    groups: {"Front End": 'fuchsia'},
    avatar: 'samuele.jpeg'
  },
  {
    name: "Filippo Biondi",
    role: "Front End Developer", // [not provided]
    groups: {"Front End": 'fuchsia'},
    avatar: 'filippo.jpg'
  },
  {
    name: "Matteo Tolloso",
    role: "Head of Back End",
    groups: {"Back End": 'yellow'},
    avatar: 'matteo.jpeg'
  },
  {
    name: "Claudia Gentili",
    role: "Back End Engineer", // [not provided]
    groups: {"Back End": 'yellow'},
    avatar: 'claudia.jpg'
  },
  {
    name: "Irene Testa",
    role: "Back End Engineer", // [not provided]
    groups: {"Back End": "yellow"},
    avatar: 'irene.jpg'
  },
  {
    name: "Francesca Poli",
    role: "Head of UX",
    groups: {"UX": 'primary'},
    avatar: 'francesca.jpeg'
  },
  {
    name: "Gianluca Morcaldi",
    role: "UI/UX Designer", // [not provided]
    groups: {"UX": 'primary'},
    avatar: 'gianluca.jpeg'
  },
  {
    name: "Giulia Ghisolfi",
    role: "UI/UX Designer", // [not provided]
    groups: {"UX": 'primary'},
    avatar: 'giulia.jpeg'
  },
  {
    name: "Simone Ianniciello",
    role: "Head of AI",
    groups: {"AI": "red", "Front End": 'fuchsia'},
    avatar: 'simone.jpg' // [not provided]
  },
  {
    name: "Bianca Ziliotto",
    role: "AI Engineer", // [not provided]
    groups: {"AI": "red"},
    avatar: 'bianca.jpeg'
  },
  {
    name: "Andrea Roncoli",
    role: "AI Engineer", // [not provided]
    groups: {"AI": "red"},
    avatar: 'andrea.jpeg'
  },
    {
    name: "Eva Johannsen",
    role: "Fron End Developer", // [not provided]
    groups: {"Front End": "fuchsia"},
    avatar: 'avatar.jpeg' // [not provided]
  },
        // Add other members similarly
      ],
    };
  },
  components: {
    MemberCard,
  },
});
</script>

<style scoped>
/* Add your styling here */
.members-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

</style>
