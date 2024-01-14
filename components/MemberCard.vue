<!-- MemberCard.vue -->

<template>
  <div class="member-card align-center justify-center ">
    <img class="ml-8" :src="require(`@/assets/avatars/${avatar}`)" alt="Avatar" />
    <div class="info">
      <h3 class='text-black' style="font-size: 2em;">{{ name }}</h3>
      <p class='text-black' style="font-size: 1.2em;">{{ role }}</p>
      <p class='text-black'>Groups: {{ groups.join(", ") }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    role: String,
    groups: Array,
    avatar: String,
  },
};
</script>

<style scoped>
/* Add your styling for the member card */
.member-card {
  background-color: white;
  margin: 20px;
  padding: 20px;
  text-align: center;
  border: 1px solid #ccc;
  border-radius: 8px;
}

.member-card img {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  margin-bottom: 10px;
}
</style>
