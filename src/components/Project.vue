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
      <v-row no-gutters>
          <v-col cols="12" xl="5" lg="5">
              <v-card color="#EBEAF7" flat style="border-radius:15px" class="ma-4 pa-2">
                  <v-row align="center"   justify="center" no-gutters>
                      <div class="pt-4">
                          <p class="text-caption  font-weight-bold ">October 1,2020</p>
                      </div>
                      <v-spacer></v-spacer>
                      <v-btn small icon plain><v-icon>mdi-dots-vertical</v-icon></v-btn>
                  </v-row>
                  <p class="text-body-1 text-center font-weight-bold">Web Designing</p>
                  <p class="text-caption grey--text text-center mt-n4">Phototyping</p>
                  <br>
                  <div class="ml-5 mr-5">
                      <v-progress-linear color="#5F5CBE" value="15"></v-progress-linear>
                  </div>
                  <v-row no-gutters>
                      <v-spacer></v-spacer>
                      <p class="text-caption font-weight-bold mr-5" style="color:#5F5CBE " >15%</p>
                  </v-row>
                  <br>  
                  <br>
                  <v-row no-gutters>
                      <v-avatar size="25"><v-img src="../assets/me.jpg"></v-img></v-avatar>
                      <v-avatar size="25" class="ml-n2"><v-img src="../assets/me.jpg"></v-img></v-avatar>
                      <v-avatar size="25" class="ml-n2"><v-img src="../assets/me.jpg"></v-img></v-avatar>   
                      <v-btn icon class="ml-2" style="background-color:#5F5CBE" small><v-icon color="white">mdi-plus</v-icon></v-btn>
                      <v-spacer></v-spacer>
                      <v-chip color="white">
                          <span style="color:#5F5CBE" class=" font-weight-bold text-caption">2 Days Left</span>   
                      </v-chip>

                  </v-row>
              </v-card>

          </v-col>
      </v-row>
  </div>
</template>

<script>
export default {
    data(){

    }
}
</script>

<style>

</style>