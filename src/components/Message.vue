<template>
  <div class="animate__animated animate__fadeIn animate__slow">
       <v-card class="pa-2" elevation="1" style="border-radius:15px;">
             <v-row align="center"   justify="center" no-gutters>
                      <div class="pt-3">
                          <p class="  font-weight-bold ">Client Messages</p>
                      </div>
                      <v-spacer></v-spacer>
                      <v-btn small icon plain><v-icon>mdi-magnify</v-icon></v-btn>
                      <v-btn small icon plain><v-icon>mdi-dots-vertical</v-icon></v-btn>
                  </v-row>
            </v-card>
            <br>
            <div style="overflow-y:scroll;height:70vh"> 
            <div class="mb-2" v-for="i in items" :key="i"  >
            <v-row class="pa-2" v-if="i.favourite==false" no-gutters align="center" justify="center">
                <v-col cols="3">
                     <v-avatar size="70">
                    <v-img :src="i.img"></v-img>
                </v-avatar>
                </v-col>
               
                <v-col cols="9">
                     <div class=" pl-2">
                     <v-row align="center" justify="center" no-gutters>
                    <p class="font-weight-bold text-caption" >{{i.title}}</p>
                    <v-spacer></v-spacer>
                   <v-btn plain @click="i.favourite=!i.favourite" icon x-small><v-rating hover    v-model="i.favourite" class="mt-n4" length="1" small></v-rating></v-btn>
                    </v-row>
                    <p class="text-caption mt-n4 grey--text">{{i.content}}</p>
                     <p style="font-size:10px;text-align:right" class="mb-n1 mt-n5">{{i.date}}</p>
                </div>
                </v-col>
            </v-row>
            <v-card v-else class="pa-2" style="border-radius:15px" hover>
                <v-row no-gutters align="center" justify="center">
                <v-col cols="3">
                     <v-avatar size="70">
                    <v-img :src="i.img"></v-img>
                </v-avatar>
                </v-col>
               
                <v-col cols="9">
                     <div class="pl-2">
                    <v-row align="center" justify="center" no-gutters>
                    <p class="font-weight-bold text-caption" >{{i.title}}</p>
                    <v-spacer></v-spacer>
                    <v-btn plain @click="i.favourite=!i.favourite" icon x-small><v-rating hover    v-model="i.favourite" class="mt-n4" length="1" small></v-rating></v-btn>
                    </v-row>
                    <p class="text-caption mt-n4 grey--text">{{i.content}}</p>
                    <p style="font-size:10px;text-align:right" class="mb-n1 mt-n5">{{i.date}}</p>
                </div>
                </v-col>
            </v-row>
            </v-card>
            </div>
            </div>
  </div>
</template>

<script>
export default {
    data(){
        return {
            items:[
                {title:'David',content:'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minima  ...',favourite:false,date:"13, October",img:"https://images.unsplash.com/flagged/photo-1570612861542-284f4c12e75f?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=870&q=80"},
                {title:'Stephanie',content:'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minima  ...',favourite:true,date:"9, October",img:"https://images.unsplash.com/photo-1499952127939-9bbf5af6c51c?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=876&q=80"},
                {title:'Jakob',content:'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minima  ...',favourite:false,date:"7, October",img:"https://images.unsplash.com/photo-1500048993953-d23a436266cf?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=869&q=80"},
                {title:'Alona',content:'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minima  ...',favourite:false,date:"5, October",img:"https://images.unsplash.com/photo-1503249023995-51b0f3778ccf?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=360&q=80"},
            ]
        }
    }
}
</script>

<style>

</style>