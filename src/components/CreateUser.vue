<template>

<form @submit.prevent="CreateUser">
<div class="container"> 
  <div class="form-group">
    <label for="name">Username</label>
    <input type="text" class="form-control" id="name" placeholder="Username" v-model="formData.name">
  </div>

  <div class="form-group">
    <label for="email">Email address</label>
    <input type="email" class="form-control" id="email" aria-describedby="emailHelp" placeholder="Enter email" v-model="formData.email">
    <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
  </div>

  <button type="submit" class="btn btn-primary">Submit</button>
  </div>
</form>

</template>

<script>
import axios from 'axios'
export default {
  name: 'CreateUser',
  data(){
      return{
        formData:{
            name: '',
            email: ''
        }
      }
  },
  methods:{
      CreateUser(){
          axios.post('http://127.0.0.1:8000/user', this.formData)
          .then(response => console.log(response))
          .catch(error => console.log(error ))
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
