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
  props: [
    'username',
    'age',
    'city',
    'followers',
    'likes',
    'photos',
    'avatar'
  ],
  computed: {
    alternative: function () {
      return 'Photo by ' + this.username;
    }
  }
};
</script>

<style scoped>

.profile-card {
  margin: 0 auto;
  margin-top: 173px;
  padding-top: 88px;
  width: 350px;
  min-height: 286px;

  text-align: center;

  background-color: var(--primary-white);
  background-image: url('~./public/images/bg-pattern-card.svg');
  background-position: 0 0;
  background-size: 350px 140px;
  background-repeat: no-repeat;
  border-radius: 12px;
  box-shadow: 1px 2px 1px 0 var(--primary-very-dark-desaturated-blue);
}

@media (max-width: 375px) {
  .profile-card {
    margin-top: 149px;
    width: 326px;
  }
}

.profile-card__avatar-wrapper {
  margin: 0 auto;
  width: 96px;
  height: 96px;

  border: 5px solid var(--primary-white);
  border-radius: 50%;
  overflow: hidden;
}

.profile-card__avatar-image {
  width: 96px;
  height: 96px;
  display: block;
}

.profile-card__title,
.profile-card__item-value {
  font-weight: bold;
  color: var(--primary-very-dark-desaturated-blue);
}

.profile-card__age,
.profile-card__city {
  color: var(--neutral-dark-gray);
}

.profile-card__age {
  font-weight: normal;
}

.profile-card__title {
  margin: 0;
  padding-top: 20px;

  letter-spacing: 0.5px;
}

.profile-card__city {
  margin: 0;
  padding-top: 13px;

  font-size: 14px;
  line-height: 14px;
}

.profile-card__list,
.profile-card__item-value {
  margin: 0;
}

.profile-card__list {
  margin-top: 23px;
  padding: 27px 24px;
  padding-bottom: 20px;
  display: flex;

  border-top: 1px solid var(--neutral-dark-gray);
}

.profile-card__item {
  width: 33%;
  display: flex;
  flex-direction: column-reverse;
}

.profile-card__item-title {
  font-size: 13px;
  line-height: 20px;
  color: var(--neutral-dark-gray);
}
</style>
