<template>
  <div align="center" class="container">
    <div class="row">
      <NewPassword></NewPassword>
      <PasswordList></PasswordList>
    </div>
    <hr>
    <div class="row">
      <PasswordDetails></PasswordDetails>
    </div>
    <hr>
  </div>
</template>

<script>
  import NewPassword from "@/components/NewPassword";
  import PasswordList from "@/components/PasswordList";
  import PasswordDetails from "@/components/PasswordDetails";

  export default {
    components: {
      NewPassword,
      PasswordList,
      PasswordDetails
    }
  }
</script>

<style>
  .container{
    margin-top: 33px;
  }
</style>
