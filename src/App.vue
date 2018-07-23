<template>
  <div id="app">
    <img src="logo.png">
    <h1>{{ msg }}</h1>
    <Profile
      v-bind:user="user"
      v-bind:avatarUrl="newAvatarUrl"
    />
  </div>
</template>

<script>

  // Import the User Profile Component
  import Profile from './components/BaseUserProfile'

export default {
  name: 'app',
  data () {
    return {
      msg: 'User Profile',
      user: null
    }
  },
  components: {
    Profile
  },
  computed:{
    newAvatarUrl(){
      return `http://c.hexotic.com${this.user.person.imageURL}`
    }
  },
  created() {
    fetch("http://c.hexotic.com/api/testUser/5733a7337e3d61136595a0c9")
      .then(response => response.json())
      .then((data) =>{
        this.user = data;
      })
  }
}
</script>

<style>
#app {
  text-align: center;
  margin-top: 60px;
}
  img{
    width:600px;
    height: 100px;
  }
</style>
