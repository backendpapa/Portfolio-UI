<template>
  <v-app>
    <v-app-bar
      app
      color="white"
      elevation="1"
      class="animate__animated animate__fadeIn animate__slower"
      
     
      
    >
      <div class="d-flex align-center mr-3">
        <p class="bold font-md mt-4">Porfolio</p>
      </div>

      
      <div class="d-flex align-center  mt-2" style="margin-left:40px" >
       <div class="d-none d-sm-flex">
         <v-text-field placeholder="Search"   solo prepend-inner-icon="mdi-magnify" @click:prepend-inner="search" style="width:30vw;border-radius:15px"  dense class="mt-3 text-caption font-weight-bold"></v-text-field>
       </div>
      </div>
      <v-spacer></v-spacer>

      <v-btn plain icon small class="mr-1"><v-icon color="#EA6334">mdi-plus-circle</v-icon></v-btn>
      <v-btn plain small icon class="mr-1"><v-icon>mdi-bell-badge-outline</v-icon></v-btn>
     <div style="height:50%">
        <v-divider   vertical></v-divider>
     </div>
     <v-avatar size="30" class="ml-2">
       <v-img src="./assets/me.jpg"></v-img>
     </v-avatar>
     <p class="text-body-2 font-weight-bold mt-3 ml-1 d-none d-sm-flex" >Backend Papa</p>
     <v-btn plain icon small> <v-icon>mdi-chevron-down</v-icon></v-btn>
    </v-app-bar>


    <div class="">
      <v-navigation-drawer
    
        
        app
        width="100"
        class=" d-none d-sm-flex"
      >
        <div style="height:15vh" >
          <!-- Icon -->
        </div>

        <v-list
          
          dense
          rounded
          
          
        >
         <p v-for="i in nav" :key="i" class="text-center"><v-btn  :to="i.to" icon><v-icon>{{i.icon}}</v-icon></v-btn></p>
         
        </v-list>
      </v-navigation-drawer>
    </div>
    <div v-if="open==true" style="position:absolute;bottom:0;right:0;top:20vh;">
     
                <div class="animate__animated animate__fadeInRight animate__delay-0.9s">
                  <v-btn
                  to="/d"
                  class="animate__animated animate__headShake "
                  color="grey"
                  fab
                  dark
                  small
                  right
                  absolute
                >
                  <v-icon >mdi-home</v-icon>
                  
                </v-btn>
                </div>
            
    </div>
     <div v-if="open==true" style="position:absolute;bottom:0;right:0;top:30vh;">
     
           
               <div class="animate__animated animate__fadeInRight animate__delay-0.7s">
                  <v-btn
                  to="/d"
                  color="grey"
                  fab
                  class="animate__animated animate__headShake "
                  dark
                  small
                  right
                  absolute
                >
                  <v-icon >mdi-account</v-icon>
                  
                </v-btn>
               </div>
              
    </div>
     <div v-if="open==true" style="position:absolute;bottom:0;right:0;top:40vh;">
     
          
               <div class="animate__animated animate__fadeInRight animate__delay-0.5s">
                  <v-btn
                  class="animate__animated animate__headShake "
                  to="/d"
                  color="grey"
                  fab
                  dark
                  small
                  right
                  absolute
                >
                  <v-icon >mdi-wechat</v-icon>
                  
                </v-btn>
               </div>
             
    </div>
    <div v-if="open==true" style="position:absolute;bottom:0;right:0;top:50vh;">
     
           
               <div class="animate__animated animate__fadeInRight animate__delay-0.3s">
                  <v-btn
                  class="animate__animated animate__headShake "
                  to="/d"
                  color="grey"
                  fab
                  dark
                  small
                  right
                  absolute
                >
                  <v-icon >mdi-calendar-text-outline</v-icon>
                  
                </v-btn>
               </div>
             
    </div>
    <div v-if="open==true" style="position:absolute;bottom:0;right:0;top:60vh;">
     
                <div class="animate__animated animate__fadeInRight animate__delay-0.1s">
                  <v-btn
                  class="animate__animated animate__headShake "
                  to="/d"
                  color="grey"
                  fab
                  dark
                  small
                  right
                  absolute
                >
                  <v-icon >mdi-clock-outline</v-icon>
                  
                </v-btn>
                </div>
             
    </div>

    <div  v-if="open==true" style="position:absolute;bottom:0;right:0;top:70vh;">
     
           
             
               <div  class="animate__animated animate__fadeInRight animate__fast ">
                  <v-btn
                
                class="animate__animated animate__headShake "
                  to="/d"
                  color="grey"
                  fab
                  dark
                  small
                  right
                  absolute
                >
                  <v-icon >mdi-cog-outline</v-icon>
                  
                </v-btn>
               </div>
       
          
    </div>
    
      <div class="" style="position:absolute;bottom:0;right:0;top:80vh;" >
      
        
                <v-btn
                  @click="open=!open"
                  color="black"
                  class="animate__animated animate__fadeIn animate__slower d-flex d-sm-none"
                  fab
                  dark
                  
                  right
                  absolute
                >
                  <v-icon v-if="open==false">mdi-chevron-up</v-icon>
                  <v-icon v-else>mdi-chevron-down</v-icon>
                </v-btn>
              
     
      </div>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import "./App.css"
export default {
  name: 'App',

  data: () => ({
    nav:[
      {title:"Home",icon:"mdi-home",to:"/d"},
      {title:"Account",icon:"mdi-account",to:"/d"},
      {title:"Home",icon:"mdi-wechat",to:"/d"},
      {title:"Calender",icon:"mdi-calendar-text-outline",to:"/d"},
      {title:"Clock",icon:"mdi-clock-outline",to:"/d"},
      {title:"Setting",icon:"mdi-cog-outline",to:"/d"},

    ],
    open:false
  }),
  methods:{
    search(){
      alert("Searching")
    }
  }
};
</script>
<style>
.bold{
  font-weight: bold;
}
.font-md{
  font-size: 20px;
}


</style>
