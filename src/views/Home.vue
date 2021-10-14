<template>
  <div>
   <v-container>
     
        <v-row no-gutters style="min-height:100vh" >
          <v-col  cols="12" xl="8" lg="8">
            <v-card style="border-radius:15px;height:100%" class="pa-5">
            <Project />
          </v-card>
          </v-col>
          <v-col cols="12" xl="4" lg="4"></v-col>
        
    </v-row>
   
   </v-container>
  </div>
</template>

<script>

import Project from '../components/Project.vue'
  export default {
    name: 'Home',

    components: {
     Project
    },
  }
</script>
