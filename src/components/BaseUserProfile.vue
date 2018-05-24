<template>
  <div class="row">
    <div class="left">
      <img src="../assets/logo.png">
      <span class="name">Cole Ditchman</span>
    </div>
    <div class="address">
      <p class="line1">1589 Wade Avenue</p>
      <p class="line2">Raleigh, North Carolina</p>
      <p class="line3">27609</p>
    </div>
  </div>

</template>

<script>
  export default {
    name: 'BaseUserProfile',
    data () {
      return {
        msg: ''
      }
    }
  }
</script>

<!-- Scoped to limit CSS to this component only -->
<style scoped>
  .row {
    border: 1px solid black;
    height: 96px;
    width: 728px;
    margin: auto;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
  }
  .left{
    display: inline-flex;
    align-items: center;
  }
  img {
    border: 4px solid #ee4494;
    width: 88px;
    height: 88px;
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
