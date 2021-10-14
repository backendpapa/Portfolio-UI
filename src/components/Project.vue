<template>
  <div>
      <v-row no-gutters>
          <p class="text-h6 font-weight-bold">Projects</p>
          <v-spacer></v-spacer>
          <p class="text-h6 grey--text">October 2021</p>
      </v-row>
      <v-row no-gutters>
          <v-col cols="10">
              <!-- stat -->
              <v-row no-gutters>
                  <v-col cols="6" xl="3" lg="3" >
                      <div>
                         <p class="text-body-1 font-weight-bold" style="color:#736FC6">45</p> 
                         <p class="text-caption mt-n4 font-weight-bold grey--text">In Progress</p>
                      </div>
                  </v-col>
                   <v-col cols="6" xl="3" lg="3">
                      <div>
                         <p class="text-body-1 font-weight-bold" style="color:#F2A684">12</p> 
                         <p class="text-caption mt-n4 font-weight-bold grey--text">In Progress</p>
                      </div>
                  </v-col>
                  <v-col cols="6" xl="3" lg="3">
                      <div>
                         <p class="text-body-1 font-weight-bold" style="color:#F6C05F">10</p> 
                         <p class="text-caption mt-n4 font-weight-bold grey--text">Upcoming</p>
                      </div>
                  </v-col>
                   <v-col cols="6" xl="3" lg="3">
                      <div>
                         <p class="text-body-1 font-weight-bold" style="color:#52F8F3">64</p> 
                         <p class="text-caption mt-n4 font-weight-bold grey--text">Total Project</p>
                      </div>
                  </v-col>
              </v-row>
          </v-col>
          <v-col cols="2">
              <v-row no-gutters>
              
                  <v-btn icon plain><v-icon>mdi-view-list-outline</v-icon></v-btn>
                  <v-btn icon plain><v-icon>mdi-view-grid</v-icon></v-btn>
              </v-row>
          </v-col>
      </v-row>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>