<template>
  <div className="tweet">
    <ProfileImage :image="user.image" />
    <div className="body">
      <div className="top">
        <User :name="user.name"
              :handle="user.handle">
        </User>/>  
        <span className="timestamp">{{timestamp}}</span>
      </div>

      <p className="message">{{message}}</p>

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

<script setup>
import ProfileImage from './ProfileImage.vue';
import User from './User.vue';

const props = defineProps({
    user:{
      name:String,
      image:String,
      handle:String
    },
    message:String,
    timestamp:String,
})

</script>

<style scoped>
a {
  color: #42b983;
}
</style>
