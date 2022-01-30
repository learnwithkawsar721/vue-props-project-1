<template>
    <section>
        <h2>User Details</h2>
        <h3>User Name:{{name}}</h3>
        <h3>User E-mail: {{ email }} </h3>
    </section>
</template>
<script>
export default {
    props:{
        name:{
            type:String,
            require:true,
        },
        email:{
            type:String,
            require:true
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
</style>