<!-- GroupMembers.vue -->
<template>
  <section
    id="contact"
    class="container gradient-blue mx-auto text-center py-12 mb-10"
  ><div class="container m-8">
        <h2
          class="w-full my-2 text-8xl font-bold leading-tight text-center text-gray-800"
        >
        About Us
        </h2>
    </div>
    <div class="members-container">
      <MemberCard
        v-for="(member, index) in groupMembers"
        :key="index"
        :name="member.name"
        :role="member.role"
        :groups="member.groups"
        :avatar="member.avatar"
      />
    </div>
  </section>
</template>

<script>
import MemberCard from "./MemberCard.vue"; // Create MemberCard.vue separately

export default {
  data() {
    return {
      groupMembers: [
        { name: "Paul Magos", role: "Project Manager", groups: ["Ux", "Backend", "Frontend"], avatar: "paul.jpeg"},
        {
    name: "Samuele Bonini",
    role: "FrontEnd Supervisor",
    groups: ["FrontEnd"],
    avatar: 'samuele.jpeg'
  },
  {
    name: "Filippo Biondi",
    role: null, // [not provided]
    groups: ["FrontEnd"],
    avatar: 'avatar.jpeg' // [not provided]
  },
  {
    name: "Matteo Tolloso",
    role: "BackEnd Supervisor",
    groups: ["BackEnd"],
    avatar: 'matteo.jpeg'
  },
  {
    name: "Claudia Gentili",
    role: null, // [not provided]
    groups: ["BackEnd"],
    avatar: 'avatar.jpeg' // [not provided]
  },
  {
    name: "Irene Testa",
    role: null, // [not provided]
    groups: ["BackEnd"],
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
    role: null, // [not provided]
    groups: ["UX"],
    avatar: 'gianluca.jpeg'
  },
  {
    name: "Giulia Ghisolfi",
    role: null, // [not provided]
    groups: ["UX"],
    avatar: 'giulia.jpeg'
  },
  {
    name: "Simone Ianniciello",
    role: "AI Supervisor",
    groups: ["AI", "FrontEnd"],
    avatar: 'simone.jpg' // [not provided]
  },
  {
    name: "Bianca Ziliotto",
    role: null, // [not provided]
    groups: ["AI"],
    avatar: 'bianca.jpeg'
  },
  {
    name: "Andrea Roncoli",
    role: null, // [not provided]
    groups: ["AI"],
    avatar: 'andrea.jpeg'
  },
    {
    name: "Eva Johannsen",
    role: null, // [not provided]
    groups: ["FrontEnd"],
    avatar: 'avatar.jpeg' // [not provided]
  },
        // Add other members similarly
      ],
    };
  },
  components: {
    MemberCard,
  },
};
</script>

<style scoped>
/* Add your styling here */
.members-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

</style>
