<template>
  <div className="tweet">
    <!--<img src="https://i.imgur.com/b0EdHVV.jpg" className="profile" alt="profile" />-->
    <ProfileImage image="user.imgage"></ProfileImage>


    <div className="body">
      <div className="top">
        <User :user="user"></User>
        <Timestamp :time="timestamp"></Timestamp>
      </div>

      <p className="message">
        {{ message }}
      </p>

      <div className="actions">
        <!-- Font Awesome icons -->
        <i class="far fa-comment"></i>
        <i class="fas fa-retweet"></i>
        <i class="far fa-heart"></i>
        <i class="fas fa-share"></i>
      </div>
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>
import ProfileImage from "./ProfileImage.vue";
import User from "./User.vue";
import Timestamp from "./Timestamp.vue";
export default {
  name: 'Tweet',
  props: {
    user: {
      name: String,
      handle: String,
    },
    timestamp: String,
    message: String,
    image: String,
  },
  components: { ProfileImage, User, Timestamp }
}
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
