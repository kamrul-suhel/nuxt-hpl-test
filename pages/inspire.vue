<template>
  <v-row>
    <v-col class="text-center">
      <img
        src="/v.png"
        alt="Vuetify.js"
        class="mb-5"
      >

      {{ name }}

      <v-btn @click="handleFetchData">Fetch data</v-btn>
      <blockquote class="blockquote">
        &#8220;First, solve the problem. Then, write the code.&#8221;
        <footer>
          <small>
            <em>&mdash;John Johnson</em>
          </small>
        </footer>
      </blockquote>
    </v-col>
  </v-row>
</template>

<script>
  import axios from 'axios'
  export default {
    data(){
      return {
        name: 'kamrul',
        age: '20'
      }
    },
    created() {
    },

    methods:{
      async handleFetchData(){
        const response = await axios.post('https://vue.hplmotors.co.uk/api/v1')
        console.log('response is: ', response.data)
      }
    }
  }
</script>
