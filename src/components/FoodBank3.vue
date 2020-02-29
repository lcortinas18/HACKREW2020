<template>
<div id="food">
  <v-app id="inspire" style="background-image: url('https://s1.1zoom.me/b5352/846/Vegetables_Pepper_Tomatoes_Onion_Potato_Cutting_518795_2560x1440.jpg'); background-position: center;">
    <v-content>
      <v-container
        fluid
        fill-height
      >
        <v-layout
          align-center
          justify-center
        >
          <v-flex
            xs12
            sm8
            md4
          >
            <v-card height="600px" width="4000px" class="elevation-12">
              <v-toolbar
                class="white--text"
                color="#4b9061"
                flat
              >
                <v-toolbar-title>Yuma County Food Bank</v-toolbar-title>
                <v-spacer></v-spacer>
              </v-toolbar>
              <v-card-actions>
                <v-row>
                  <v-col>
                    <v-img src="https://secure.feedingamerica.org/images_logos/FoodBankLogo_603_275w.jpg">
                    </v-img>
                  </v-col>
                  <v-col>
                    <v-row>
                    <font size="5" font-style="Verdana">1400 Independence Ave SW, Washington, DC 20250</font>
                    </v-row>
                    <v-row class="py-12">
                      <font size="4" font-style="Verdana">(800) 795-3272</font>
                    </v-row>
                  </v-col>
                </v-row>
                <v-spacer></v-spacer>
                <v-btn class="white--text" color="#4b9061">Confirm</v-btn>

              </v-card-actions>
            </v-card>
          </v-flex>
        </v-layout>
      </v-container>
    </v-content>
  </v-app>
</div>
</template>>

<script>
//import Vue from 'vue'
//import App from './App.vue'
//import DonationForm from './components/DonationForm.vue'
//import vuetify from './plugins/vuetify';

export default {
  name: 'FoodBank1',
  
  components: {
  },

  methods:{
          
  },

  data: () => ({
    //
  }),
};
</script>