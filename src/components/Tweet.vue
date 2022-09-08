<template>
  <div className="tweet">
    <ProfileImage :image="user.image"/>

    <div className="body">
      <div className="top">
        <User :userData="{name:user.name,handle:user.handle}"/>
        <Timestamp :time="timestamp"/>
      </div>

      <p className="message">
        {{message}}
      </p>

      <Actions/>
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
  name:"Tweet",
  props: ["user","timestamp","message"],
  components: {ProfileImage, User, Timestamp, Message, Actions}
}
</script>
<style scoped>
a {
  color: #42b983;
}
</style>
