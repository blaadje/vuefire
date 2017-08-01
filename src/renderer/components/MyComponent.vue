<template lang="pug">
  div
    pre {{ anArray }}
    ul
      li(v-for="user in users").
        {{ user.name }} 
</template>

<script>
import Firebase from 'firebase'

var config = {
  apiKey: 'AIzaSyBz73_KOl_AYMfeJnBQ7lBCyH-KuSUQsqQ',
  authDomain: 'projet-tets.firebaseapp.com',
  databaseURL: 'https://projet-tets.firebaseio.com',
  projectId: 'projet-tets',
  storageBucket: 'projet-tets.appspot.com',
  messagingSenderId: '304277615671'
}
var firebaseApp = Firebase.initializeApp(config)
var db = firebaseApp.database()

export default {

  firebase () {
    return {
      users: db.ref('users')
    }
  }

}
</script>

<style></style>
