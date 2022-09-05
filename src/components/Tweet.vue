<template>
  <div className="tweet">
    <!--<img src="https://i.imgur.com/b0EdHVV.jpg" className="profile" alt="profile" />-->
    <ProfileImage image="user.imgage"></ProfileImage>


    <div className="body">
      <div className="top">
        <User :user="user"></User>
        <Timestamp :time="timestamp"></Timestamp>
      </div>
      <Message :message="message"></Message>
      <Actions></Actions>
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>
import ProfileImage from "./ProfileImage.vue";
import User from "./User.vue";
import Timestamp from "./Timestamp.vue";
import Message from "./Message.vue";
import Actions from "./Actions.vue";
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
  components: { ProfileImage, User, Timestamp, Message, Actions }
}
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
