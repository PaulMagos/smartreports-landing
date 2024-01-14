<!-- MemberCard.vue -->
<template>
  <div class="member-card gradient align-center justify-center">
    <img class="ml-8" :src="local_avatar" alt="Avatar" />
    <h3 class='text-white' style="font-size: 1.8em;">{{ local_name }}</h3>
    <!-- <p class='text-white' style="font-size: 1.1em;">{{ local_role }}</p> -->
    <!-- <UBadge class="mb-2" v-if="local_name.startsWith('Filippo')" color="green" size="md" style="font-size: 1em;" variant="solid">Best Employee</UBadge>
    <UBadge class="mb-2" v-if="local_name.startsWith('Matteo')" color="green" size="md" style="font-size: 1em;" variant="solid">Best Employee</UBadge>
    <UBadge class="mb-2" v-if="local_name.startsWith('Simone')" color="green" size="md" style="font-size: 1em;" variant="solid">Best Employee</UBadge> -->
    <UBadge v-if="local_role!='Project Manager' && !local_role.startsWith('Head')" color="blue" size="md" style="font-size: 1em;" variant="soft">{{ local_role }}</UBadge>
    <UBadge class="mb-4" v-if="local_role=='Project Manager'" color="teal" size="md" style="font-size: 1em;" variant="soft">{{ local_role }}</UBadge>
    <UBadge v-if="local_role.startsWith('Head')" color="amber" size="md" style="font-size: 1em;" variant="soft">{{ local_role }}</UBadge>
    <br>
    <UBadge
      v-if="local_groups"
      class="mt-2"
      :label="group"
      v-for="i, group in user.local_groups"
      :key="i"
      variant="subtle"
      :color="i"
      style="bottom: -2%; position: relative;"
      size="md" :ui="{ rounded: 'rounded-full' }"
      ></UBadge>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'MemberCard',
  data() {
    return {
      user: {
        local_name: this.name,
        local_role: this.role,
        local_groups: this.groups,
        local_avatar: this.avatar,
      },
    }
  },
  props: {
    name: String,
    role: String | null,
    groups: {} | null,
    avatar: String,
  },
  computed: {
    local_name() {
      return this.user.local_name
    },
    local_role() {
      return this.user.local_role
    },
    local_groups() {
      return this.user.local_groups 
    },
    local_avatar() {
      return `./${this.user.local_avatar}`
    },
  }
});
</script>

<style scoped>
/* Add your styling for the member card */

.member-card {
  background: linear-gradient(60deg, rgb(150, 190, 220) 10%, rgb(15, 80, 150) 5%, rgb(15, 80, 120) );
  margin: 10px;
  padding: 12px;
  text-align: center;
  border: 1px solid #ccc;
  border-radius: 20px;
  overflow: hidden; /* Ensure the overflow is hidden for the gradient effect */
  position: relative; /* Add position relative for absolute positioning of the hover effect */
}

.member-card:hover {
  background: linear-gradient(60deg, rgb(200, 232, 255) 10%, rgb(26, 103, 190) 5%, rgb(26, 103, 190)); /* Change the gradient colors for hover */
}

.member-card img {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  /* margin-bottom: 10px; */
  z-index: 2; /* Ensure the image is above the hover effect */
}
</style>
