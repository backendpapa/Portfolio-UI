<template>
  <div>
   <v-container>
     
        <div class="d-sm-none d-md-flex">
          <v-row class="d-none d-sm-flex" no-gutters style="height:85vh"  >
          <v-col  cols="12" xl="8" lg="8">
            <v-card elevation="1" style="border-radius:15px;  " class="pa-5">
            <Project />
          </v-card>
          </v-col>
          <v-col cols="12" xl="4" lg="4" class="pl-3">
            <Message />
          </v-col>
        
    </v-row>
        </div>
    <div class="d-flex d-sm-none">
      <div style="width:100%" >
       <v-tabs-items v-model="tab">
        <v-tab-item v-for="item in items" :key="item.tab">
          <v-card class="pa-2"  elevation="1" :color="tab==0?'':'#F9FAFD'" style="" >
            
              <component class="" v-bind:is="item.content"></component>
           
          </v-card>
          
        </v-tab-item>
      </v-tabs-items>
    </div>
    </div>
        <div style="width:100%" class="d-none d-sm-flex d-md-none">
          <div style="width:100%" >
       <v-tabs-items class="" v-model="tab">
        <v-tab-item v-for="item in items" :key="item.tab">
          <v-card class="pa-2"  elevation="1" :color="tab==0?'':'#F9FAFD'" style="" >
            
              <component class="" v-bind:is="item.content"></component>
           
          </v-card>
          
        </v-tab-item>
      </v-tabs-items>
          </div>
    </div>
   
   </v-container>
  </div>
</template>

<script>

import Project from '../components/Project.vue'
import Message from '../components/Message.vue'
  export default {
    name: 'Home',

    components: {
     Project,
     Message
    },
    data(){
    return {
      tab:0,
      items:[{content:"Project",tab:"Project"},{content:'Message',tab:"Message"}]
    }
    }
  }
</script>
