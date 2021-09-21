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
          <td>{{ user.firstName }}</td>
          <td>{{ user.lastName }}</td>
          <td>{{ user.email }}</td>
          <td>{{ user.phoneNumber }}</td>
        </tr>
      </table>
    </div>
 
</template>

<script>
export default {
  el: "#usersinfo",
  props: {
    users: Object,
  },
};
</script>

<style>
table {
  font-family: arial, sans-serif;
  border-collapse: collapse;
  width: 100%;
}
b{
    margin: 3%;
}
td, th {
  border: 1px solid #dddddd;
  text-align: left;
  padding: 8px;
}

tr:nth-child(even) {
  background-color: #bd8383;
}
</style>