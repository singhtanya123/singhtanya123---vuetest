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
  name: "userform",
  data(){
    return {
      firstName:'',
      lastName:'',
      email:'',
      phoneNumber:'',
    };
  },
  methods:{
    onSubmit(e){
      e.preventDefault();
      if(!this.firstName){
        alert("Please enter your firstname");
      }
      if(!this.lastName){
        alert("Please enter your lastName");
      }
      if(!this.email){
        alert("Please enter your email");
      }
      if(!this.phoneNumber){
        alert("Please enter your phoneNumber");
      }
      const newTask ={
        id:Math.floor(Math.random()),
        firstname:this.firstName,
        lastname:this.lastName,
        email:this.email,
        phone:this.phoneNumber
      };
      console.log(newTask);
      this.$emit ("user-form",newTask);
      this.firstName="",
      this.lastName=""
      this.email="",
      this.phoneNumber="";
    },
  },
 
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
  justify-content: center;    
  margin-right: 3%;
}
input {
  padding: 1%;
}
.save-btn {
  background-color: blue;
  padding: 10px;
  margin-left: 2%;
}
</style>
