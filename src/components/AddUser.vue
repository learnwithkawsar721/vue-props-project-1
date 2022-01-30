<template>
    <section>
        <h2>Add New User</h2>
        <form @submit.prevent="submitUser">
            <label>UserName:</label>
            <input type="text" v-model="enterUserName">
            <label>User E-mail:</label>
            <input type="email" v-model="enterUserEmail">
            <button>Add New</button>
        </form>
    </section>
</template>

<script>
export default {
    emits:['add-user'],
   data(){
       return{
           enterUserName:'',
           enterUserEmail:''
       }
   },

   methods:{
       submitUser(){
           this.$emit('add-user',this.enterUserName,this.enterUserEmail);
           this.enterUserName ="";
           this.enterUserEmail="";
       }
   }
}
</script>

<style scoped>
section{
    border: 1px solid #ccc;
    width: 50%;
    margin: 2rem auto;
    padding: 3rem;
    border-radius: 20px;
    box-shadow: 2px 0px 4px #000;
}
label{
    font-size: 20px;
    display: inline-block;
}
input{
    padding: 10px;
    display: inline-block;
    margin: 20px;
    border-radius: 10px;
}
button{
    display: block;
    margin: 0 auto;
    padding: 10px 15px;
    border-radius: 10px;
    background-color: rgb(128, 0, 49);
    color: #fff;
    cursor: pointer;
}
</style>
