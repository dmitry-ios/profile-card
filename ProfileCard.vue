<template>
  <article>
    <img v-bind:src="avatar" v-bind:alt="alternative" width="96" height="96">
    <p>{{username}} <span>{{age}}</span></p>
    <p>{{city}}</p>
    <dl>
      <dt>Followers</dt>
      <dd>{{followers}}</dd>
      <dt>Likes</dt>
      <dd>{{likes}}</dd>
      <dt>Photos</dt>
      <dd>{{photos}}</dd>
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
