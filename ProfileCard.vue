<template>
  <article class="profile-card">
    <div class="profile-card__avatar-wrapper">
      <img class="profile-card__avatar-image" v-bind:src="avatar" v-bind:alt="alternative" width="96" height="96">
    </div>
    <p class="profile-card__title">{{username}} <span class="profile-card__age">{{age}}</span></p>
    <p class="profile-card__city">{{city}}</p>
    <dl class="profile-card__list">
      <div class="profile-card__item">
        <dt class="profile-card__item-title">Followers</dt>
        <dd class="profile-card__item-value">{{followers}}</dd>
      </div>
      <div class="profile-card__item">
        <dt class="profile-card__item-title">Likes</dt>
        <dd class="profile-card__item-value">{{likes}}</dd>
      </div>
      <div class="profile-card__item">
        <dt class="profile-card__item-title">Photos</dt>
        <dd class="profile-card__item-value">{{photos}}</dd>
      </div>
    </dl>
  </article>
</template>

<script>
export default {
  data: function () {
    return {
      username: 'Victor Crest',
      age: '26',
      city: 'London',
      followers: '80K',
      likes: '803K',
      photos: '1.4K',
      avatar: 'images/image-victor.jpg'
    };
  },
  computed: {
    alternative: function () {
      return 'Photo by ' + this.username;
    }
  }
};
</script>

<style scoped>

</style>
