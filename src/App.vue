<template>
  <div id="app">
    <h2>{{emailGen}}</h2>
    <!-- <h3>{{getEmail()}}</h3> -->
    <h2>LISTA EMAILS</h2>
    <ul v-if="listEmail.length >= 10">
      <li v-for="(element, index) in listEmail" :key="index">
        <!-- <p>{{element}}</p> -->
        <Email :email="element"/>
      </li>
    </ul>
  </div>
</template>

<script>
import axios from 'axios'

import Email from './components/emails'

export default {
  name: 'App',
  data: function() {
    return {
      listEmail: [],
      emailGen: '',
    }
  },

  components: {
    Email,
  },

  mounted() { 
    for (let i = 0; i < 10; i++)
    {
      axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
      .then((response) => {
        this.listEmail.push(response.data.response);
      });
    }
        // axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        // .then(res => {
        //   console.log(res.data);
        // });
        // axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        // .then((response) => {
        //   this.listEmail.push(response.data.response);
        // });
        // axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        // .then((response) => {
        //   this.listEmail.push(response.data.response);
        // });
        // axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        // .then((response) => {
        //   this.listEmail.push(response.data.response);
        // });axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        // .then((response) => {
        //   this.listEmail.push(response.data.response);
        // });axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        // .then((response) => {
        //   this.listEmail.push(response.data.response);
        // });axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        // .then((response) => {
        //   this.listEmail.push(response.data.response);
        // });axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        // .then((response) => {
        //   this.listEmail.push(response.data.response);
        // });axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        // .then((response) => {
        //   this.listEmail.push(response.data.response);
        // });axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        // .then((response) => {
        //   this.listEmail.push(response.data.response);
        // });axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        // .then((response) => {
        //   this.listEmail.push(response.data.response);
        // });
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

