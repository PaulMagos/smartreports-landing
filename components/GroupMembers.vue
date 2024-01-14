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

export default defineComponent({
  name: "GroupMembers",
  data() {
    return {
      groupMembers: [
        { name: "Paul Magos", role: "Project Manager", groups: ["UX", "Back End", "Front End"], avatar: "paul.jpeg"},
        {
    name: "Samuele Bonini",
    role: "Front End Supervisor",
    groups: ["Front End"],
    avatar: 'samuele.jpeg'
  },
  {
    name: "Filippo Biondi",
    role: "Front End Developer", // [not provided]
    groups: ["Front End"],
    avatar: 'avatar.jpeg' // [not provided]
  },
  {
    name: "Matteo Tolloso",
    role: "Back End Supervisor",
    groups: ["Back End"],
    avatar: 'matteo.jpeg'
  },
  {
    name: "Claudia Gentili",
    role: "Back End Engineer", // [not provided]
    groups: ["Back End"],
    avatar: 'avatar.jpeg' // [not provided]
  },
  {
    name: "Irene Testa",
    role: "Back End Engineer", // [not provided]
    groups: ["Back End"],
    avatar: 'avatar.jpeg' // [not provided]
  },
  {
    name: "Francesca Poli",
    role: "UX Supervisor",
    groups: ["UX"],
    avatar: 'francesca.jpeg'
  },
  {
    name: "Gianluca Morcaldi",
    role: "UI/UX Designer", // [not provided]
    groups: ["UX"],
    avatar: 'gianluca.jpeg'
  },
  {
    name: "Giulia Ghisolfi",
    role: "UI/UX Designer", // [not provided]
    groups: ["UX"],
    avatar: 'giulia.jpeg'
  },
  {
    name: "Simone Ianniciello",
    role: "AI Supervisor",
    groups: ["AI", "Front End"],
    avatar: 'simone.jpg' // [not provided]
  },
  {
    name: "Bianca Ziliotto",
    role: "AI Engineer", // [not provided]
    groups: ["AI"],
    avatar: 'bianca.jpeg'
  },
  {
    name: "Andrea Roncoli",
    role: "AI Engineer", // [not provided]
    groups: ["AI"],
    avatar: 'andrea.jpeg'
  },
    {
    name: "Eva Johannsen",
    role: "Fron End Developer", // [not provided]
    groups: ["Front End"],
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
