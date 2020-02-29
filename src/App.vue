<template>
<div id="app">
  <v-app>
    <v-content>
      <section id="hero">
        <v-row no-gutters>
          <v-img
            :min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
            src="https://s1.1zoom.me/b5352/846/Vegetables_Pepper_Tomatoes_Onion_Potato_Cutting_518795_2560x1440.jpg"
          >
            <v-theme-provider dark>
              <v-container fill-height>
                <v-row
                  align="center"
                  class="white--text mx-auto"
                  justify="center"
                >
                  <v-col
                    class="white--text text-center"
                    cols="12"
                    tag="h1"
                  >
                    <span
                      class="font-weight-light"
                      :class="[$vuetify.breakpoint.smAndDown ? 'display-1' : 'display-2']"
                    >
                      WELCOME TO
                    </span>

                    <br>

                    <span
                      :class="[$vuetify.breakpoint.smAndDown ? 'display-3': 'display-4']"
                      class="font-weight-black"
                    >
                      WeFood
                    </span>

                  </v-col>

                  <v-btn
                    class="align-self-end"
                    fab
                    outlined
                    @click="$vuetify.goTo('#donation')"
                  >
                    <v-icon>mdi-chevron-double-down</v-icon>
                  </v-btn>
                </v-row>
              </v-container>
            </v-theme-provider>
          </v-img>
        </v-row>
      </section>

      <section id="donation">
        <div class="py-12"></div>
        <v-container class="text-center">
          <h2 class="display-2 font-weight-bold mb-3">YOU ARE...</h2>
          <v-row align="center">
        <v-col cols="12" sm="6">
          <div class="my-12">
            <div class="py-12">
              <v-btn 
              color="#4b9061" 
              fab 
              x-large dark>
                <v-icon>mdi-domain</v-icon>
              </v-btn>
            </div>
          </div>
        </v-col>
          <div width=100px>
              <v-btn size ="" 
              color="#5668EC"
              @click="donatorPage()" 
              fab 
              x-large dark>
                <v-icon>mdi-account-circle</v-icon>
              </v-btn>
            </div>
      </v-row>

          <div></div>
        </v-container>

        <div class="py-12"></div>
      </section>
    </v-content>
  </v-app>
 </div>
</template>

<script>
import Vue from 'vue'
//import App from './App.vue'
import DonationForm from './components/DonationForm.vue'
import vuetify from './plugins/vuetify';

export default {
  name: 'App',
  
  components: {
  },

  methods:{
          
          donatorPage(){
            new Vue({
              vuetify,
              render: h => h(DonationForm)
              }).$mount('#app')
              this.dialog=false;
           }
  },

  data: () => ({
    //
  }),
};
</script>