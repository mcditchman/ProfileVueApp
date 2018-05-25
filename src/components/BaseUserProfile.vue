<template>
  <div class="row">
    <div class="left">
      <img :class="user.person.gender" v-bind:src="avatarUrl">
      <span class="name">{{`${user.person['given-name']} ${user.person['family-name']}`}}</span>
    </div>
    <div class="address">
      <p class="line1">{{`${user.person.address['street-number']} ${user.person.address['street-name']}`}}</p>
      <p class="line2">{{`${user.person.address.city}, ${user.person.address.state}`}}</p>
      <p class="line3">{{user.person.address.zip}}</p>
    </div>
  </div>

</template>

<script>
  export default {
    name: 'BaseUserProfile',
    props: {
      user: Object,
      avatarUrl: String
    }
  }
</script>

<!-- Scoped to limit CSS to this component only -->
<style scoped>
  .row {
    border: 1px solid #ababab;
    height: 96px;
    width: 728px;
    margin: auto;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    box-shadow: 3px 4px #d4d4d4;
  }
  .left{
    display: inline-flex;
    align-items: center;
  }
  img {
    width: 88px;
    height: 88px;
  }
  .male{
    border: 4px solid #37d5fe;
  }
  .female{
    border: 4px solid #ee4494;
  }
  .name {
    font-family: "Arial Bold";
    font-size: 36px;
    margin-left: 10px;
  }
  .address {
    top: auto;
    font-family: "Arial Regular";
    font-size: 18px;
    margin-right: 19px;
  }
  .address p{
    margin: 2px 0px 2px 0px;
  }
</style>
