<template>
  <div class="hello">
    <p>{{ contenu }}</p>
  </div>
</template>
<script>

// exporte le composant pour Webpack
export default {
  name: 'message', // identifiant au composant
  props: {
    contenu: {
      type: String, // restriction sur l'heritage de propriétés
      default: function(){
        return 'blabla...'
      }
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