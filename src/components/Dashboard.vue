<template>
  <div>
      <UserForm/>
  </div>
</template>

<script>
import UserForm from './UserForm.vue';
export default {
    name:'Dashboard',
    props: {
    firstName: String,
    lastName: String,
    emailId: String,
    phoneNumber: Number
  },
  components:{
      UserForm
  }
}
</script>

<style>

</style>