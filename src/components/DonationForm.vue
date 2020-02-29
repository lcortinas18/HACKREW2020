<template>
<v-app style="background-image: url('https://s1.1zoom.me/b5352/846/Vegetables_Pepper_Tomatoes_Onion_Potato_Cutting_518795_2560x1440.jpg'); background-position: center;">
<v-container id="app" >
  <v-layout 
    align-center
    justify-center>

<v-sheet class="justify-center"
        id="contact"
        color="#333333"
        dark
        elevation="4"
        max-width="700px"
        tag="section"
        tile
      >
        <div class="py-12"></div>

        <v-container>
          <h1 class="display-2 font-weight-bold mb-3 text-uppercase text-center">Donation Amount</h1>

          <v-responsive
            class="mx-auto mb-12"
            width="56"
          >
            <v-divider class="mb-1"></v-divider>

            <v-divider></v-divider>
          </v-responsive>

          <v-theme-provider light>
            <v-row no-gutters>
              <v-col cols="12">
                <v-text-field
                  flat
                  append-icon="mdi-food-apple"
                  type=number
                  v-model="produce"
                  label="Produce in lbs."
                  solo
                ></v-text-field>
              </v-col>

              <v-col cols="12">
                <v-text-field
                  flat
                  append-icon="mdi-food"
                  type=number
                  v-model="meat"
                  label="Meat in lbs."
                  solo
                ></v-text-field>
              </v-col>

              <v-col cols="12">
                <v-text-field
                  flat
                  append-icon="mdi-food-croissant"
                  type=number
                  v-model="grains"
                  label="Grains in lbs."
                  solo
                ></v-text-field>
              </v-col>

              <v-col cols="12">
                <v-text-field
                  flat
                  append-icon="mdi-map-marker"
                  type=number
                  v-model="zip"
                  label="Zipcode"
                  solo
                ></v-text-field>
              </v-col>

              <v-col
                class="mx-auto"
                cols="auto"
              >
                <v-btn
                  color="accent"
                  x-large
                  @click="match()"
                >
                  Match
                </v-btn>
              </v-col>
            </v-row>
          </v-theme-provider>
        </v-container>

        <div class="py-12"></div>
      </v-sheet>
  </v-layout>
</v-container>
</v-app>
</template>

<script>

import Vue from 'vue'
//import App from '../App.vue'
import FoodBank1 from './FoodBank1.vue'
import FoodBank2 from './FoodBank2.vue'
import FoodBank3 from './FoodBank3.vue'
import vuetify from '../plugins/vuetify';

export default {
  name: 'DonationForm',
  
  components: {
    
  },

  methods: {
    match(){
           if(this.produce > 50) { 
            new Vue({
              vuetify,
              el: '#app',
              render: h => h(FoodBank1)
              })
              this.dialog=false;
           }

           else if(this.zip == 20001 || this.zip == 20020 || this.zip == 20032){ 
            new Vue({
              vuetify,
              el: '#app',
              render: h => h(FoodBank2)
              })
              this.dialog=false;
           }

           else if(this.produce <= 50 && this.meat <= 50 && this.grains <= 50){ 
            new Vue({
              vuetify,
              el: '#app',
              render: h => h(FoodBank3)
              })
              this.dialog=false;
           }

           else{print}
    }

  },

  data() {
      return {
        produce:"",
        meat:"",
        grains:"",
        zip:""
      };
  },

  
};
</script>
