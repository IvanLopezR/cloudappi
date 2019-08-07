<template>

    <div>
        <h1>{{ title }}</h1>
        <ul v-if="users && users.length">
            <li v-for="user of users">
            <p><strong>{{user.name}}</strong></p>
            <p>{{user.email}}</p>
            </li>
        </ul>
    </div>

</template>

<script>

import axios from 'axios';

export default {
    props:{
        title: String
    },
  data() {
    return {
      users: [],
      errors: []
    }
  },

  created() {
    axios.get(`https://my-user-manager.herokuapp.com/users`)
    .then(response => {
      this.users = response.data
    })
    .catch(e => {
      this.errors.push(e)
    })
  }
}

</script>

<style scoped>
h1 {
  margin: 40px 0 30px;
  color: #F28E3C;
}
ul {
  list-style-type: none;
}
li {
  display: inline-block;
  margin: 0 50px;
  color: #4EBCD4;
}
</style>