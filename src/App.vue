<template>
  <div id="app" class = "container">
    <div class = "page-header">
      <h3> Sample of Vuejs and Firebase </h3>
    </div>


  </div>
</template>

<script>
import Hello from './components/Hello'
import Firebase from 'firebase'

  let config = {
    apiKey: "AIzaSyDugllzf_oFKox4C3_2-RC554rehWo3sik",
    authDomain: "test-vue-01.firebaseapp.com",
    databaseURL: "https://test-vue-01.firebaseio.com",
    projectId: "test-vue-01",
    storageBucket: "test-vue-01.appspot.com",
    messagingSenderId: "508488863934"
  }
let app =  Firebase.initializeApp(config);
let db = app.database();
let whoSend = db.ref('who');

export default {
  name: 'app'
  Firebase : {
    who : whoSend
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
