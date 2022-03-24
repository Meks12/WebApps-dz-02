<template>
<v-app id="app">

  <v-container>
  
    <v-text-field
      label="Upisi ime osobe"
      color="primary"
      v-model="input"
      @keypress.enter="show">
  
       <template v-slot:append>
  
          <v-btn
            depressed 
            tile
            color="primary"
            class="ma-0"
            @click="show">
          
            show
            
          </v-btn>
        
      </template>
        
    </v-text-field>
      
  </v-container>
  
</v-app>


</template>



<script>

  import axios from 'axios';
  import HelloWorld from '../components/HelloWorld'
  import func from 'vue-editor-bridge';


  export default {
    name: 'HomevieW',
    data: function() {
      return {
        comitovi: [],
      };
      
    },
    

  async mounted(){

  let agify = await axios.get("https://api.agify.io?name=Nikola")
                              .then(response => this.totalVuePackages
                               = response.data.total);

  let genderize = await axios.get("https://api.genderize.io?name=Nikola")
                                .then(response => this.totalVuePackages
                                = response.data.total);
  
  let nationalize = await axios.get("https://api.nationalize.io?name=Nikola")
                                .then(response => this.totalVuePackages
                                = response.data.total);

  let gotov1 = await response1.json();
  let gotov2 = await response2.json();
  let gotov3 = await response3.json();

  this.comitovi = gotov1;
  this.comitovi = gotov2;
  this.comitovi = gotov3;



  console.log(agify);
  console.log(genderize);
  console.log(nationalize);



  

  }, 
  
  }