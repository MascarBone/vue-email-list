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

  // methods: {
  //   getEmail() {


  //     axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
  //       .then((response) => {
  //         this.emailGen = response.data.response;
  //         console.log(this.emailGen);
  //         this.listEmail.push(response.data.response);
  //         console.log(this.listEmail);
  //       });
  //     // while (this.listEmail.length < 10)
  //     // {
        
  //     //   axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
  //     //   .then((response) => {
  //     //     this.listEmail.push(response.data.response);
  //     //     console.log(this.listEmail);
  //     //   });
  //     // }
  //   }
  // },

  mounted() { 
    // const self = this;
    // let i = 0;

        axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        .then((response) => {
          this.listEmail.push(response.data.response);
        });
        axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        .then((response) => {
          this.listEmail.push(response.data.response);
        });
        axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        .then((response) => {
          this.listEmail.push(response.data.response);
        });axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        .then((response) => {
          this.listEmail.push(response.data.response);
        });axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        .then((response) => {
          this.listEmail.push(response.data.response);
        });axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        .then((response) => {
          this.listEmail.push(response.data.response);
        });axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        .then((response) => {
          this.listEmail.push(response.data.response);
        });axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        .then((response) => {
          this.listEmail.push(response.data.response);
        });axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        .then((response) => {
          this.listEmail.push(response.data.response);
        });axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
        .then((response) => {
          this.listEmail.push(response.data.response);
        });
        
      // while (this.listEmail.length < 10)
      // {

        // i++;
      // }
      // axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
      // .then((response) => {

      //   this.listEmail.push(response.data.response);       
      //   console.log(this.listEmail);
      //   console.log(this.listEmail.length);

      //   this.listEmail.push(response.data.response);       
      //   console.log(this.listEmail);
      //   console.log(this.listEmail.length);

      //   this.listEmail.push(response.data.response);       
      //   console.log(this.listEmail);
      //   console.log(this.listEmail.length);

      // })


// while (i < 10)
      // {
      //   console.log('ciao');
      //   console.log(axios);
      //   console.log(this.listEmail);
      //   i++;
      // }
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

