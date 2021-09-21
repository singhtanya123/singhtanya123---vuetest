<template>
  <div>
    <h3>Users Data</h3>
    <table>
      <tr>
        <th>FirstName</th>
        <th>LastName</th>
        <th>Email</th>
        <th>PhoneNumber</th>
      </tr>

      <tr :key="user.id" v-for="user in users">
        <td>{{ user.name.firstname }}</td> 

        <td>{{ user.name.lastname }}</td>
        <td>{{ user.email }}</td>
        <td>{{ user.phone }}</td>
        <button ><router-link to="/userform"></router-link>Edit </button>
        <button @click="$emit('delete-task', user.id)">Delete</button>
      </tr>
    </table>
  </div>
</template>

<script>
// import Vue from "vue";
// import VueRouter from "vue-router";
// import Dashboard from './Dashboard.vue';
// import UserForm from './UserForm.vue';

// Vue.use(VueRouter);
// const router = new VueRouter({
//   routes: [
//     { path: "/", name: "dashboard", component: Dashboard },
//     { path: "/userform", name: "userform", component: UserForm },
//   ],
// });
export default {
  el: "#usersinfo",
//  router,
//  components: { Dashboard, UserForm },
  props: {
    users: Object,
  },
  emits:["delete-task"],
  methods: {
    onEdit(id) {
      console.log(id);
 //     this.$router.push({ name: "UserForm", params: { id: id } });
    },
  },
};
</script>

<style>
table {
  font-family: arial, sans-serif;
  border-collapse: collapse;
  width: 100%;
  border: 1px solid #dddddd;
}
b {
  margin: 3%;
}
th {
  text-align: left;
  padding: 8px;
}
td {
  text-align: left;
  padding: 8px;
}
tr:nth-child(even) {
  background-color: #bd8383;
}
button{
        padding: 1%;
        float: right;
        margin: 2%;
        background-color: crimson;
    }
</style>