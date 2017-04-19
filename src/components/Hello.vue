<template>
  <div class="hello">
    <h1>Hello in the new world {{ prenom }}!</h1>
    <p>Your are wild {{ majuscule }} !</p>
    <textarea v-model="contenu"></textarea>
    <input v-model="langage"></textarea>
    <user :langage="langage"></user>

    <message :contenu="contenu"></message>
    <message :contenu="contenu"></message>
    <message></message>
    <message></message>


  </div>
</template>

<script>
// import le composant 'User' depuis le fichier User.vue
import User from './User.vue';
import Message from './Message.vue';

// exporte le composant pour Webpack
export default {

  name: 'hello', // identifiant au composant
  components: {
    user: User,
    message: Message
  }, // je charge le composant User dans Hello
  data () {
    return {
      contenu: '',
      langage: 'JS',
      msg: 'Welcome to Your Vue.js App',
      prenom: 'Julien'
    }
  },
  computed: {
    majuscule: function(){
      return this.prenom.toUpperCase();
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1,
  h2 {
    font-weight: normal;
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