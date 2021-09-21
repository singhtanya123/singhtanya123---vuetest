<template>
  <div>
    <!--open close of new create user button-->
    <Button
      @show-user-form="showUserForm"
      :text="createUser ? 'Close' : 'Create User'"
      :color="createUser ? 'red' : 'green'"
    ></Button>
    <!--form will be show when button is clicked-->
    <div v-if="createUser" class="main">
      <UserForm @user-form="addUser"/>
    </div>

    <UsersInfo :users="users" />
  </div>
</template>

<script>
import UserForm from "./UserForm.vue";
import Button from "./Button.vue";
import UsersInfo from "./UsersInfo.vue";
export default {
  name: "Dashboard",
  props: {
    firstName: String,
    lastName: String,
    emailId: String,
    phoneNumber: Number
  },
  components: {
    UserForm,
    Button,
    UsersInfo,
  },
  data() {
    return {
      users: [],
      createUser: false,
    };
  },
  methods: {
    showUserForm() {
      this.createUser = !this.createUser;
    },
    addUser(user) {
      this.users = [...this.users, user];
  },
  },
  created() {
    this.users = [
      { 
        id: '1',
        firstName: "Leanne ",
        lastName: "Graham",
        email: "Sincere@april.biz",
        phoneNumber: "1-770-736-8031 x56442",
      },
      {
        id:'2',
        firstName: "Ervin ",
        lastName: "Howell",
        email: "Sincere@april.biz",
        phoneNumber: "1-770-736-8031 x56442",
      },
      { 
        id: '3',
        firstName: "Eren",
        lastName: "jager",
        email: "Sincere@april.biz",
        phoneNumber: "1-770-736-8031 x56442",
      },
      { 
        id: '4',
        firstName: "Naruto",
        lastName: "Chan",
        email: "Sincere@april.biz",
        phoneNumber: "1-770-736-8031 x56442",
      },
      { 
        id:'5',
        firstName: "sakura ",
        lastName: "flower",
        email: "Sincere@april.biz",
        phoneNumber: "1-770-736-8031 x56442",
      },
      { 
        id: '6',
        firstName: "Sukana",
        lastName: "yuji",
        email: "Sincere@april.biz",
        phoneNumber: "1-770-736-8031 x56442",
      },
    ];
  },
}
</script>

<style>
.main {
  border: 5px white solid;
  height: 50%;
  width: 100%;
}
</style>