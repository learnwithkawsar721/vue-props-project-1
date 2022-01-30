<template>
  <section>
    <user-details :name="user.name" :email="user.email"></user-details>
    <add-user @add-user="addNewUser"></add-user>
  </section>
</template>

<script>
import AddUser from "./components/AddUser.vue";
import UserDetails from "./components/UserDetails.vue";

export default {
  name: "App",
  components: {
    AddUser,
    UserDetails,
  },
  data() {
    return {
      user: {
        name:"kawsar",
        email:'kawsar@gmail.com'
      },
    };
  },
  methods:{
    addNewUser(name,email){
      this.user.name = name;
      this.user.email = email;
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
