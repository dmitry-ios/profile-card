<template>
  <div class="app-container">
    <profile-card
      username="Victor Crest"
      age="26"
      city="London"
      followers="80K"
      likes="803K"
      photos="1.4K"
      avatar="images/image-victor.jpg"
    >
    </profile-card>
  </div>
</template>

<script>
import ProfileCard from "./ProfileCard.vue";

export default {
  components: {
    ProfileCard,
  },
};
</script>

<style scoped>
.app-container {
  padding-top: 173px;
}

@media (max-width: 375px) {
  .app-container {
    padding-top: 149px;
  }
}
</style>
