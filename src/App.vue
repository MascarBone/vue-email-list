<template>
  <div id="app">
    <ul>
      <li v-for="(element, index) in listEmail" :key="index">
        <p>{{element}}</p>
      </li>
    </ul>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'App',

  data: function() {
    return {
      listEmail: [],
    }
  },

  components: {
  },


  mounted() { 
    const self = this;
    let i = 0;

    while (self.listEmail.length < 2 && i < 10)
    {
      axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
      .then(function(response) {

        console.log(response.data.response);
        
        self.listEmail.push(response.data.response)

        console.log(self.listEmail);


      })
      
      i++;
    }
    // console.log('ciao');
    // console.log(axios);
    console.log(self.listEmail);
  },
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>

