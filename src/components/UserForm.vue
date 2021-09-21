<template>
  <div>
    <form @submit="onSubmit" class="form-submit">
      <div class="form-control">
        <label class="task-label">Enter your first name </label>
        <input
          type="text"
          name="firstName"
          placeholder="Enter your first name"
          v-model="firstName"
        />
      </div>
      <div class="form-control">
        <label class="task-label">Enter your last name </label>
        <input
          type="text"
          name="lastName"
          placeholder="Enter your last name"
          v-model="lastName"
        />
      </div>
      <div class="form-control">
        <label class="task-label">Enter your email Id </label>
        <input
          type="text"
          name="email"
          placeholder="Enter your email Id"
          v-model="email"
        />
      </div>
      <div class="form-control">
        <label class="task-label">Enter your mobile number </label>
        <input
          name="phoneNumber"
          placeholder="Enter your mobile number"
          v-model="phoneNumber"
        />
      </div>
      <input type="submit" value="Save Task" class="save-btn" />
    </form>
  </div>
</template>

<script>
export default {
  el: "#userform",
};
</script>

<style scoped>
.form-submit {
  margin-bottom: 15px;
}
.form-control {
  padding: 2%;
}
.task-label {
  margin: 2%;
  justify-content: center;
}
input {
  padding: 1%;
}
.save-btn {
  background-color: green;
  padding: 10px;
  margin: 3%;
}
</style>
