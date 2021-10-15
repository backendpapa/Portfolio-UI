<template>
  <div>
      <v-row no-gutters class="ma-4">
          <p class="text-h6 font-weight-bold">Projects</p>
          <v-spacer></v-spacer>
          <p class="text-h6 grey--text">October 2021</p>
      </v-row>
      <v-row no-gutters class="ma-4">
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
     <div style="overflow-y:scroll;height:60vh">
          <v-row no-gutters >
          <v-col cols="12" xl="5" lg="6" sm="6" v-for="i in items" :key="i">
              <v-card hover  :color="i.colorbg"  style="border-radius:15px" class="ma-4 pa-2">
                  <v-row align="center"   justify="center" no-gutters>
                      <div class="pt-4">
                          <p class="text-caption  font-weight-bold ">{{i.date}}</p>
                      </div>
                      <v-spacer></v-spacer>
                      <v-btn small icon plain><v-icon>mdi-dots-vertical</v-icon></v-btn>
                  </v-row>
                  <p class="text-body-1 text-center font-weight-bold">{{i.title}}</p>
                  <p class="text-caption grey--text text-center mt-n4">{{i.subtitle}}</p>
                  <br>
                  <div class="ml-5 mr-5">
                      <v-progress-linear :color="i.ccolor2" :value="i.value"></v-progress-linear>
                  </div>
                  <v-row no-gutters>
                      <v-spacer></v-spacer>
                      <p class="text-caption font-weight-bold mr-5" :style="i.color3" >{{i.value}}%</p>
                  </v-row>
                  <br>  
                  <br>
                  <v-row no-gutters>
                      <v-avatar size="25"><v-img src="../assets/me.jpg"></v-img></v-avatar>
                      <v-avatar size="25" class="ml-n2"><v-img src="../assets/me.jpg"></v-img></v-avatar>
                      <v-avatar size="25" class="ml-n2"><v-img src="../assets/me.jpg"></v-img></v-avatar>   
                      <v-btn icon class="ml-2"  :style="i.color" small><v-icon color="white">mdi-plus</v-icon></v-btn>
                      <v-spacer></v-spacer>
                      <v-chip color="white">
                          <span :style="i.color3" class=" font-weight-bold text-caption">{{i.time}}</span>   
                      </v-chip>

                  </v-row>
              </v-card>

          </v-col>
      </v-row>
     </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
            items:[
                {title:"Web Designing",subtitle:"Phototyping",date:"October 1,2021",time:"2 Days Left",color:"background-color:#5F5CBE",ccolor2:"#5F5CBE",colorbg:"#EBEAF7",value:15,color3:"color:#5F5CBE"},
                {title:"Mobile App",subtitle:"Shopping",date:"October 5,2021",time:"3 Weeks Left",color:"background-color:#EA6334",ccolor2:"#EA6334",colorbg:"#FDEFE9",value:30,color3:"color:#EA6334"},
                {title:"Dashboard",subtitle:"Medical",date:"October 16,2021",time:"2 Weeks Left",color:"background-color:#F2A638",ccolor2:"#F2A638",colorbg:"#FEF6E8",value:30,color3:"color:#F2A638"},
                {title:"Web Designing",subtitle:"Wireframing",date:"October 20,2021",time:"3 Weeks Left",color:"background-color:#6994FA",ccolor2:"#6994FA",colorbg:"#F0F4FE",value:30,color3:"color:#6994FA"},
            ],
            hover:false
        }
    }
}
</script>

<style>

</style>