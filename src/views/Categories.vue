

<template>
  <h1>Finanzen</h1>
  <p v-for="user in users" :key="user.id">{{user.name}}</p>
</template>

<script>
import userData from "./users.json"

export default {
  data () {
    return {users: userData}
  }
}
</script>