<template>
  <v-app>
    <v-app-bar
      app
      color="white"
      elevation="1"
     
      
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
     <v-btn plain icon> <v-icon>mdi-chevron-down</v-icon></v-btn>
    </v-app-bar>


    <div class="d-none d-sm-flex">
      <v-navigation-drawer
    
        expand-on-hover
        app
        mini-variant-width="100"
        class=" d-none d-sm-flex"
      >
        <v-list>
          <v-list-item class="px-2">
            <v-list-item-avatar>
              <v-img src="https://randomuser.me/api/portraits/women/85.jpg"></v-img>
            </v-list-item-avatar>
          </v-list-item>

          <v-list-item link>
            <v-list-item-content>
              <v-list-item-title class="text-h6">
                Sandra Adams
              </v-list-item-title>
              <v-list-item-subtitle>sandra_a88@gmail.com</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list
          nav
          dense
        >
          <v-list-item link>
            <v-list-item-icon>
              <v-icon>mdi-folder</v-icon>
            </v-list-item-icon>
            <v-list-item-title>My Files</v-list-item-title>
          </v-list-item>
          <v-list-item link>
            <v-list-item-icon>
              <v-icon>mdi-account-multiple</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Shared with me</v-list-item-title>
          </v-list-item>
          <v-list-item link>
            <v-list-item-icon>
              <v-icon>mdi-star</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Starred</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
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
    //
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
