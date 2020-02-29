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
                <v-toolbar-title>Bread For the City</v-toolbar-title>
                <v-spacer></v-spacer>
              </v-toolbar>
              <v-card-actions>
                <v-row>
                  <v-col>
                    <v-img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBxIREhUTERIWFhUXFRoYGRcXFxUYGRkZFxcXFxYXGhcaICggGCAlGxUWITEhMSkrLi4uFx8zODMtNygtLisBCgoKDg0OGxAQGy8lICUtLS0tKy0tLS0wLy0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLf/AABEIAOEA4QMBEQACEQEDEQH/xAAcAAEAAgIDAQAAAAAAAAAAAAAABgcEBQECAwj/xABFEAABAwIEAggDBQUGBAcAAAABAAIDBBEFEiExBlEHEyIyQWFxgRSRoSNCUnKxFTOSssEkYoLC0eFTotLwFyU0VHOjs//EABoBAQACAwEAAAAAAAAAAAAAAAABAgMEBQb/xAAyEQEAAgIBAwIEBAUEAwAAAAAAAQIDEQQSITEFQRMiUXEyM2GBFSNCkaEUNFKxwfDx/9oADAMBAAIRAxEAPwCNrM8aICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICDlBwhqQIacoOEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEGdg2GPqpmQx95x3OwA1c4+gSZ0y4MU5LxWFyYVhFDh4LQ5jXOAzOkeMzreNnGw3O1ljmZeixYMOCNdt/qYvwtRVrc2VoJHZlisD63Gj/e6b0ZeLhzRvX7wp3HMJkpJnQyixGx8HN8HDyP+oV4ns89nw2xXmstepYRAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEEo6OXOFWcnfMEuX82UEfoos3/AE+f5k686lG6hz3OJlJL7nMXXzZvG9/G6mGnebTaery96bEZo25Y5XtaXB1muIGZpuHAeBuBqmoWpmvXtWUk4qxB1ZRUtTIAJGySQutoHaNcHeW23mVWPLd5V5y4K5J870iCs5ogICAgICAgICAgICAgICAgICAgICAgICDNwfEXU00czN2OvbmNnD3BIUSy4ck47xaFjY5wpDiTBWUTw18guQe487EG3ccDod9Rt4qsTry7GbiV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">
                    </v-img>
                  </v-col>
                  <v-col>
                    <v-row>
                    <font size="5" font-style="Verdana">4900 Puerto Rico Ave NE, Washington, DC 20017</font>
                    </v-row>
                    <v-row class="py-12">
                      <font size="4" font-style="Verdana">(202) 644-9800</font>
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
  name: 'FoodBank2',
  
  components: {
  },

  methods:{
          
  },

  data: () => ({
    //
  }),
};
</script>